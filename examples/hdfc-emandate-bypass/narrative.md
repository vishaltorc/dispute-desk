---
title: Worked example — e-mandate cancelled, charge processed anyway (narrative)
type: example
status: fully synthetic — every name, amount, date, and reference number below is invented for illustration; resemblance to any real case is incidental
illustrates: category B classification, deflections D1/D2/D3, the chargeback demand, evidence packaging
last_verified: 2026-06-10
---

# Worked example: the e-mandate that wouldn't die

> **This is an illustration, not a precedent.** It shows how the repo's pieces — classification, gates, templates, evidence formats — fit together on one coherent fact pattern. It does not suggest that any step here produces any particular result in another case. All data is synthetic.

## The fact pattern

"R" holds an HDFC credit card ending **4321** (synthetic). In January, R subscribes to a streaming service, **STREAMCO**, on a monthly e-mandate of **₹1,499**.

- **05 Jan** — R cancels the e-mandate through the bank's card-controls app and receives an in-app confirmation (mandate reference `MNDT-0001`, synthetic).
- **03 Feb** — the statement shows a fresh debit: `STREAMCO MUMBAI — ₹1,499` dated 01 Feb. No pre-debit notification was received before it.
- R's first reaction is the common one: complain to the merchant. STREAMCO's support replies that billing "is handled by the payment partner". Dead end.

## Classification (the step that shaped everything after)

Walking [classification.md](../../procedure/classification.md): R *did* authorise the original relationship — so not category A. The charge is recurring, the mandate was cancelled before the debit, and no pre-debit notice arrived — **category B**, on two independent grounds (post-withdrawal debit; missing notification). The complaint will cite the [e-mandate framework entry](../../regulations/rbi/recurring-payments-emandate.md) and name the cancelled-recurring network dispute category.

What classification avoided: filing this as "fraud" (it isn't — the relationship was real, and a fraud filing would have triggered card blocking and the wrong investigation track, per deflection D4's logic), or as a vague "billing complaint" (which loses both the framework hook and the network category).

## The complaint and what came back

- **04 Feb** — Initial dispute filed using [template 01](../../banks/hdfc/templates/01-initial-dispute.md) with the category-B paragraph: cancellation date, method, mandate reference, the missing pre-debit notification, statement extract attached. Reference obtained: `CC-0000001` (synthetic). Gates G0/G1 passed before sending.
- **18 Feb** — Bank reply #1: *"Please cancel the mandate with the merchant to avoid future charges."* — textbook [deflection D1](../../banks/hdfc/known-deflections.md). The mandate was already cancelled, with proof, before the debit.
- **19 Feb** — Deflection rejected using [template 02](../../banks/hdfc/templates/02-reject-deflection.md): cancellation proof re-cited as exhibit E2, the unanswered question asked plainly — *on what basis was a post-withdrawal debit processed?*
- **27 Feb** — Bank reply #2: *"No debit was processed on the mandate, as it stands cancelled."* — [deflection D2](../../banks/hdfc/known-deflections.md) with a twist of D3: technically the *mandate* wasn't debited; the merchant had charged the card-on-file directly, bypassing the cancelled mandate.
- **28 Feb** — Counter filed: the statement line is the bank's own record (E1); the e-mandate framework governs recurring debits regardless of the rail the merchant used, and on withdrawal the merchant was required to delete stored card details. Simultaneously — because "the mandate is cancelled but the charge stands" is exactly the cancelled-recurring pattern — a formal **chargeback demand** went in using [template 03](../../banks/hdfc/templates/03-chargeback-demand.md), naming the network's cancelled-recurring dispute category and noting the dispute window.

## Where it went

The chargeback demand changed the conversation: it asked for a yes-with-date or a no-in-writing-with-rule, neither of which a form reply could supply. The L2 escalation that followed (SLA lapse on the rejection, gate G3 met) attached the complete indexed pack — six exhibits, one timeline table — and the case resolved at that rung with a credit and a fee-reversal follow-up via [template 07](../../banks/hdfc/templates/07-amount-correction.md). *(In this synthetic telling, resolution at L2 is a narrative choice to keep the example short — it is not a representation of how far any real case must or will go.)*

The chronology is in [timeline.md](timeline.md); the transferable lessons are in [what-worked.md](what-worked.md).
