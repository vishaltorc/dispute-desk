---
title: Decision tree — from user state to the single correct next step
type: procedure
scope: an AI walks this with the user; every external step is precondition-gated
last_verified: 2026-06-10
---

# Decision tree

Match the user's situation to a state below. Each state yields **one correct next step**, the template to use, and the gates that must pass first ([preconditions.md](preconditions.md)). If two states seem to match, the more specific one wins. If none match, interview the user until one does — do not improvise a path.

Templates referenced are HDFC's (`banks/hdfc/templates/`); for another bank, the same-numbered template in its folder.

## How to read a state

```
STATE — how the user typically describes it
→ NEXT STEP (recipient level) | TEMPLATE | GATES
```

---

### S0 — "I just found a charge I want to dispute" (nothing filed yet)

First: classify ([classification.md](classification.md)).

- **S0a — category A (unauthorised):**
  → File the dispute **immediately** (L1) | [01-initial-dispute](../banks/hdfc/templates/01-initial-dispute.md) | gates G0, G1.
  Reporting delay changes the user's liability — same-day filing matters ([liability entry](../regulations/rbi/unauthorised-transactions-liability.md)). Also follow the bank's card-blocking guidance for actual fraud; for *suspected-but-unsure*, see S8 first.
- **S0b — category B (cancelled mandate / recurring charged anyway):**
  → File the dispute (L1) | [01-initial-dispute](../banks/hdfc/templates/01-initial-dispute.md) | gates G0, G1.
  The complaint cites the e-mandate framework ([entry](../regulations/rbi/recurring-payments-emandate.md)) and demands the charge be treated under it.
- **S0c — category C (service/billing, merchant reachable):**
  → One written merchant attempt with a deadline (rung 0) — then L1 with proof of that attempt | [01-initial-dispute](../banks/hdfc/templates/01-initial-dispute.md) | gates G0, G1.
- **S0d — category D (amount error / duplicate / promised refund not received):**
  → File at L1 | [01-initial-dispute](../banks/hdfc/templates/01-initial-dispute.md) (for missing refunds the ask is the credit; for a wrong refund amount already received, use [07-amount-correction](../banks/hdfc/templates/07-amount-correction.md)) | gates G0, G1.

### S1 — "I complained, they gave me a reference, nothing has happened yet" (SLA still running)

→ **Wait the SLA out; build the package.** No external send. | no template | —
Assemble [timeline table](../templates-shared/timeline-table.md) and [evidence index](../templates-shared/evidence-index.md) so the escalation is ready the day the SLA lapses. Diarise the lapse date. *Exception:* if the network chargeback window closes before the SLA (gate G3 exception) → S4 now.

### S2 — "The bank replied with something that doesn't address my complaint" (deflection)

Typical lines: "please cancel the mandate yourself", "no debit found", "block your card first", a re-sent older reply.
→ Reject the deflection in writing at the **same rung** | [02-reject-deflection](../banks/hdfc/templates/02-reject-deflection.md) | gates G0–G2; check the reply against [known-deflections](../banks/hdfc/known-deflections.md) and cite the matching counter.
A deflection rejected in writing converts into a G3 escalation trigger if repeated.

### S3 — "SLA expired / they closed it without fixing it" (escalation up one rung)

→ Escalate **one** rung (L2 if coming from L1; L3 if from L2) | [04-pno-escalation](../banks/hdfc/templates/04-pno-escalation.md) only when the next rung is PNO, otherwise [02-reject-deflection](../banks/hdfc/templates/02-reject-deflection.md) restructured per the bank ladder (`banks/hdfc/escalation-ladder.md` names the right template per rung) | gates G2, G3 (+ G4 from L3 up).

### S4 — "The bank won't raise a chargeback / says it's between me and the merchant"

→ Formal chargeback demand at the current rung | [03-chargeback-demand](../banks/hdfc/templates/03-chargeback-demand.md) | gates G0–G2.
The demand names the applicable network dispute category ([Visa](../regulations/networks/visa-reason-codes.md) / [Mastercard](../regulations/networks/mastercard-reason-codes.md) / [RuPay](../regulations/networks/rupay-dispute-rules.md)) and the window date. The issuing bank is the user's only door into the network dispute system — "deal with the merchant" is not a complete answer for network-eligible categories (see known-deflections).

### S5 — "Bank says the merchant responded/proved the charge and re-applied it" (representment)

→ Rebut the representment with evidence, at the rung where the chargeback was handled | [06-merchant-representment-rebuttal](../banks/hdfc/templates/06-merchant-representment-rebuttal.md) | gates G0–G3 + **demand a copy of the merchant's representment documents** if not provided — the rebuttal must answer what the merchant actually submitted, not a guess.

### S6 — "They refunded, but the amount is wrong / fees and interest from the disputed charge weren't reversed"

→ Amount-correction request at the rung that issued the credit | [07-amount-correction](../banks/hdfc/templates/07-amount-correction.md) | gates G0, G2.
The ask itemises: principal, late fees, interest, GST on fees, and (category A) the liability rule the itemisation rests on.

### S7 — "PNO level done — SLA lapsed or final rejection in hand"

→ **Boundary of this repo (v1).** | no template | gate G5.
Tell the user plainly: the internal ladder is exhausted; the RBI Ombudsman scheme exists with its own preconditions and time limits ([reference entry](../regulations/rbi/ombudsman-scheme-2021.md)); read the scheme document at the official source before acting. Do not walk the filing. Help them keep the complete case file intact — it is exactly what any next forum will need.

### S8 — "I'm not sure this charge is fraud — I might have authorised something"

→ **Classify before filing anything** ([classification.md](classification.md)) | no template | gate G1.
Filing "fraud" for an authorised-but-disputed charge can trigger card blocking and an investigation track that doesn't fit the facts; filing "billing dispute" for genuine fraud surrenders the liability-window protections. Interview, classify, then go to S0.

### S9 — "It's been charged again this cycle while the dispute is open" (recurring continues)

→ Two-part step at current rung: (a) add the new debit to the open complaint (same reference — do **not** open a fresh complaint), (b) if category B, demand mandate-level stoppage citing the e-mandate framework | [02-reject-deflection](../banks/hdfc/templates/02-reject-deflection.md) with the new debit in the timeline | gates G0, G2.

---

## Rules for walking the tree

1. **One state, one step.** Never fire two escalations in parallel rungs; never combine a chargeback demand with a rung-skip.
2. **Gates are blocking.** If a named gate fails, use the refusal pattern in [preconditions.md](preconditions.md) — name the gate, the gap, and the path to meet it.
3. **Re-enter at the top after every bank response.** Each reply moves the user to a new state; re-match rather than assuming the old path continues.
4. **The repo stops at S7.** Anything beyond the bank's internal ladder is out of scope in v1.
