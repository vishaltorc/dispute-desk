---
title: Preconditions — what must be true before each step
type: procedure
scope: gates for every step in the decision tree and escalation ladder
last_verified: 2026-06-10
---

# Preconditions

Every externally-facing step (anything that sends a complaint or escalation to the bank) is gated. An AI assistant using this repo must check the relevant gate **before** producing a draft, and must refuse — explaining which precondition is unmet and how to meet it — rather than draft around a missing gate. The user being angry, or time feeling short, does not open a gate. (If a *chargeback window* is genuinely closing, that changes which step is urgent — it does not skip a gate; see G3.)

## G0 — Facts captured (gate for everything)

All of the following, from the user, before any draft:

- [ ] The transaction as it appears on the statement: date, merchant descriptor, amount, currency.
- [ ] Card last-4 digits (never the full number — refuse it if offered).
- [ ] What makes it disputed, in one sentence, in the user's words.
- [ ] Any prior contact with bank or merchant: dates, channels, reference numbers, outcomes.
- [ ] Whether the card is still active, and whether the charge is one-off or recurring.

**Unmet →** interview the user (see HOW_AI_SHOULD_USE_THIS.md, interview pattern). Do not proceed on a partial fact set; a draft with holes invites closure on a technicality.

## G1 — Classification done (gate for the first complaint)

- [ ] The dispute has been classified per [classification.md](classification.md) and the classification stated to the user with its consequence.
- [ ] If category A (unauthorised): the user has been told the reporting-delay liability rule and the complaint is being filed **immediately** — this category is time-critical (see [the liability entry](../regulations/rbi/unauthorised-transactions-liability.md)).
- [ ] If category B (cancelled recurring/e-mandate): proof of cancellation (or of the missing pre-debit notification) is identified, even if not yet exported.
- [ ] If category C (service/billing with reachable merchant): one written merchant attempt exists or a stated reason why it would be futile.

**Unmet →** classify first. The category decides the rules, the template, and the deadline math. A wrong category is worse than a late complaint.

## G2 — Reference number captured (gate for every escalation past L1)

- [ ] An L1 complaint exists with a bank-issued **reference number**, captured verbatim.
- [ ] The date it was filed and the SLA stated (or the bank's published L1 SLA) are known.

**Unmet →** file at L1 first, or — if L1 was filed but no reference was given — the next step is a reference-number demand at L1, not an escalation. Higher rungs evaluate "was the rung below exhausted"; without a reference number nothing below is provable.

## G3 — Escalation trigger met (gate for moving up any rung)

One of:

- [ ] The current rung's SLA has lapsed (filed date + `sla_days` from `banks/<bank>/contacts.md` < today), **or**
- [ ] The bank closed/replied with a written outcome that is factually wrong or matches an entry in `banks/<bank>/known-deflections.md` (quote it in the escalation), **or**
- [ ] The bank's reply resolves a different question than the complaint asked (note the mismatch explicitly).

**Unmet →** wait out the SLA while assembling the evidence pack (`templates-shared/evidence-index.md`). Escalating early gives the higher rung a procedural reason to bounce the complaint back down.

**Exception — closing chargeback window:** if the network dispute window (see `regulations/networks/`) would lapse before the current rung's SLA, do not wait silently: the correct step is the [chargeback demand template](../banks/hdfc/templates/03-chargeback-demand.md) at the **current** rung, stating the window date. The window is a reason to act at the rung you are on — never a reason to skip one.

## G4 — Escalation package complete (gate for L3 and above)

- [ ] Timeline table built (`templates-shared/timeline-table.md`) — every event dated, referenced, sourced.
- [ ] Evidence pack indexed (`templates-shared/evidence-index.md`) — numbered, each item named in the index.
- [ ] Every prior reference number and every bank reply (quoted or attached) included.
- [ ] The ask is identical to the original complaint (or the delta is explained, e.g. accrued late fees added with dates).

**Unmet →** build the package first. At PNO level the file is read cold by someone new; the package *is* the case.

## G5 — Internal ladder exhausted (boundary gate — v1 stops here)

- [ ] PNO (or the bank's highest published internal level) responded inadequately or its SLA lapsed, with references and dates in hand.

**Met →** this repo's guidance ends. The RBI Ombudsman route exists ([reference entry](../regulations/rbi/ombudsman-scheme-2021.md)) with its own strict preconditions and time limits; the user should read the scheme at its official source. v1 deliberately does not walk the filing. An AI must say this plainly rather than improvise filing guidance.

---

## Refusal pattern (for the AI)

When a gate is unmet, the refusal must name the gate, the missing item, and the path to meet it:

> "I can't draft the PNO escalation yet: gate G3 isn't met — HDFC's L2 SLA of {{N}} days runs until {{DATE}} and there's no written closure from them. Escalating today gives them a procedural reason to bounce it. While we wait, let's build the evidence index so the escalation is ready to send the day the SLA lapses."
