---
title: Universal escalation ladder (bank-agnostic)
type: procedure
scope: any Indian bank, card disputes
last_verified: 2026-06-10
---

# The universal escalation ladder

Indian bank grievance redressal is a **strict ladder**. Skipping a rung is the most common procedural way to lose a valid dispute: the higher rung (and ultimately the RBI Ombudsman) checks whether the rungs below were exhausted, and bounces complaints that skipped them. Climb in order, document every rung, and only climb when the rung below has actually failed (trigger met).

Bank-specific recipients, addresses, and exact SLAs live in `banks/<bank>/escalation-ladder.md` and `banks/<bank>/contacts.md`. This file defines the universal shape.

> **Parallel clock warning:** card-network chargeback rights run on their **own** clock (typically measured from the transaction or expected-service date — see `regulations/networks/`). The grievance ladder does not pause that clock. If the dispute is chargeback-eligible, the chargeback must be demanded early (rung 1–2), not after the ladder is exhausted.

## Rung 0 — Merchant (conditional)

- **Trigger:** the dispute is about service/goods/billing with a reachable, legitimate merchant (see [classification.md](classification.md), category C/D).
- **Skip when:** the transaction is unauthorised, the merchant is unreachable/abusive, or a cancelled mandate was bypassed — go straight to rung 1.
- **What to do:** one written attempt with a stated deadline; keep the proof. Card networks often expect an attempt-to-resolve-with-merchant for service disputes, and it strengthens every later rung.
- **Do not accept as resolution:** verbal promises without a reference or date.

## Rung 1 — Bank customer service (L1)

- **Trigger:** you have a disputed transaction and your facts captured (gate G1 in [preconditions.md](preconditions.md)).
- **Recipient:** the bank's published card customer-service channel (`banks/<bank>/contacts.md`, level L1).
- **What to include:** the [initial dispute template](../banks/hdfc/templates/01-initial-dispute.md) content — transaction line as it appears on the statement, the category you classified, the specific ask, the evidence index.
- **Non-negotiable output of this rung:** a **complaint reference number**. No reference number = the complaint does not exist for every later rung. Ask for it explicitly; note date, channel, and the agent's stated SLA.
- **Do not accept as resolution:** "we have noted your concern" without a reference; advice to "contact the merchant" when the category does not require it; closure without a written reason.

## Rung 2 — Grievance / escalation desk (L2)

- **Trigger:** L1's stated SLA expired with no resolution, **or** L1 closed the complaint with a reason that is wrong on facts or is a known deflection (`banks/<bank>/known-deflections.md`).
- **Recipient:** level L2 in `banks/<bank>/contacts.md`.
- **What to include:** L1 reference number, the L1 outcome (quote it), why it is inadequate, the timeline table (`templates-shared/timeline-table.md`), the original ask restated.
- **Do not accept as resolution:** a re-send of the L1 reply; a new reference number that resets the clock without addressing the complaint; a partial credit presented as full resolution.

## Rung 3 — Senior grievance / priority redressal (L3, where the bank publishes one)

- **Trigger:** L2 SLA expired or L2 response repeats the deflection.
- **Recipient:** level L3 in `banks/<bank>/contacts.md`.
- **What to include:** everything in rung 2 plus the L2 reference and response; the evidence pack as an indexed attachment (`templates-shared/evidence-index.md`).
- **Do not accept as resolution:** anything not in writing.

## Rung 4 — Principal Nodal Officer (PNO)

- **Trigger:** the rungs below are exhausted (references + expired SLAs in hand) and the complaint is still unresolved or wrongly closed.
- **Recipient:** the PNO in `banks/<bank>/contacts.md`. The PNO is the bank's RBI-facing complaints owner; this is the last internal rung.
- **What to include:** the full, chronological case — every reference number, every bank reply quoted, the timeline table, the indexed evidence pack, the single specific ask, and a clear statement that this is the final internal escalation before regulator-level remedies.
- **Do not accept as resolution:** verbal assurances; "we are looking into it" past the stated SLA; resolution of a *different* complaint than the one made.

## Rung 5 — RBI Ombudsman (out of scope, v1)

The Reserve Bank - Integrated Ombudsman Scheme 2021 exists above the ladder ([reference entry](../regulations/rbi/ombudsman-scheme-2021.md)) and its core precondition is exactly this ladder: the bank must have rejected the complaint or failed to resolve it within the scheme's waiting period, and the filing must be within its time limit. **This repo deliberately does not cover the filing process in v1** — premature or malformed Ombudsman complaints are the top cause of non-maintainability dismissals. When rung 4 is genuinely exhausted, the user should read the scheme document at its official source before doing anything.

---

## Ladder-wide rules

1. **One rung at a time, in writing, with references.** Every email carries the prior reference numbers.
2. **SLA discipline:** note the bank's stated SLA at each rung; escalate when it lapses, not before (the higher rung will ask).
3. **Same complaint, consistent story:** the facts, amount, and ask must be identical at every rung. Changing numbers mid-ladder is how complaints get re-opened as "new" and clocks reset.
4. **Everything that matters, in the email body or an indexed attachment** — not in a phone call. Calls are fine for status checks; they are not evidence.
