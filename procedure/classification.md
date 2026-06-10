---
title: Classification — picking the correct dispute category
type: procedure
scope: maps a fact pattern to a category; the category decides the applicable rules
last_verified: 2026-06-10
---

# Classification

The single highest-leverage decision in a card dispute is made in the first email: **what category is this?** The category determines which RBI framework applies, which network reason-code family fits, what the deadlines are, and what the bank is obliged to do. Misclassification is silent — the bank will happily process a wrongly-categorised complaint to a dead end.

**Plain-English summaries below are for navigation — verify every rule against the linked regulation entry and its official source before relying on it.** No category implies any particular outcome.

## The first question: did the cardholder authorise *this* debit?

Not "is the charge fair" — **was this specific debit made with the cardholder's authority?**

| | Cardholder authorised this debit | Cardholder did not authorise this debit |
|---|---|---|
| **One-off charge** | Category **C** (service/billing) or **D** (amount error) | Category **A** (unauthorised) |
| **Recurring charge** | C/D — unless the mandate was cancelled or the pre-debit notice was missing → Category **B** | Category **A** (and check B: a never-consented mandate is both) |

## Category A — Unauthorised electronic transaction

**Fact pattern:** the user did not make, authorise, or share credentials for this debit. Card lost/stolen/skimmed, OTP phished, account-takeover, or a debit with no customer action at all.

**Why it matters:** RBI's customer-protection framework on unauthorised electronic transactions governs ([entry](../regulations/rbi/unauthorised-transactions-liability.md)) — it ties the customer's maximum liability to **how quickly the debit is reported**, places the burden of proving customer negligence on the bank, and sets resolution timelines. The clock starts at the user's knowledge of the debit.

**Consequences of choosing A:**
- File immediately; every day of reporting delay can change the liability band.
- The bank's fraud track applies; expect card block/reissue.
- The complaint should say "unauthorised electronic transaction" in those words and cite the entry above — *not* "billing dispute", which routes it away from the liability framework.

**Risk of overusing A:** if the user did authorise the underlying relationship (e.g. signed up, then got charged more than expected), filing it as fraud misroutes the case, can void the better-fitting category-B/C rights, and damages credibility for the rest of the ladder. When in doubt, interview (decision-tree S8).

## Category B — Recurring charge after cancellation / e-mandate non-compliance

**Fact pattern:** a subscription or e-mandate the user once authorised, but: the user cancelled (mandate, subscription, or card-on-file consent) and was charged anyway; or no pre-debit notification arrived as required; or the charge bypassed the mandate framework entirely (e.g. merchant charged a "saved card" directly after mandate cancellation).

**Why it matters:** RBI's e-mandate framework for recurring card transactions ([entry](../regulations/rbi/recurring-payments-emandate.md)) sets the conditions for recurring debits — registration with additional-factor authentication, pre-debit notification, and the right to withdraw the mandate. Separately, the card networks maintain a dispute category specifically for **cancelled recurring transactions** ([Visa](../regulations/networks/visa-reason-codes.md) · [Mastercard](../regulations/networks/mastercard-reason-codes.md) · [RuPay](../regulations/networks/rupay-dispute-rules.md)), which gives the issuing bank a concrete chargeback path.

**Consequences of choosing B:**
- The complaint cites the framework entry *and* names the cancelled-recurring network category — two independent hooks instead of zero.
- Proof of cancellation (or absence of the pre-debit notice) becomes the core evidence; the evidence pack is built around it.
- "Take it up with the merchant" is an incomplete answer here — the network category exists precisely for this pattern (see `banks/<bank>/known-deflections.md`).

**B vs A boundary:** charged *after a valid cancellation* is B (the original relationship was authorised). A mandate the user *never set up at all* is A. State which one in the complaint.

## Category C — Authorised but disputed (service / billing)

**Fact pattern:** the user made or authorised the transaction, but: goods/services not delivered, not as described, cancelled-but-charged (one-off, not mandate), or a promised refund never arrived ("credit not processed").

**Why it matters:** this is primarily a merchant-dispute path. The network reason-code families for "credit not processed" / "services not provided" apply ([networks index](../regulations/networks/)); networks generally expect an attempt to resolve with the merchant first, and the dispute window typically runs from the transaction or expected-delivery date.

**Consequences of choosing C:**
- Rung 0 (written merchant attempt) is usually a real precondition — see gate G1.
- The chargeback window is the binding deadline; track it from day one (gate G3 exception).
- The bank's role is to raise the network dispute correctly, not to adjudicate the service quality itself.

## Category D — Amount error / duplicate / refund-amount mismatch

**Fact pattern:** right merchant, wrong number: double charge, wrong amount captured, currency conversion error, or a refund issued for less than agreed; disputed-charge late fees and interest not reversed after resolution.

**Why it matters:** these are processing-error claims — usually the cleanest evidence (two statement lines, or the agreed figure vs the credited figure) and the most arithmetic-driven asks.

**Consequences of choosing D:**
- The complaint is an itemised reconciliation: what was charged, what should have been, the delta, including consequential fees/interest/GST on fees ([07-amount-correction](../banks/hdfc/templates/07-amount-correction.md)).
- Duplicate/processing-error network codes apply rather than fraud or service codes.

## Stating the classification

The first complaint should carry one sentence of the form:

> "This is a dispute of an **[unauthorised electronic transaction / recurring debit after mandate cancellation / authorised transaction where the service was not provided / processing error]**, and I request it be handled under the applicable framework."

An AI assistant must state the chosen category and its consequence to the user before drafting, and record it — the category must stay consistent across every rung (escalation-ladder rule 3).
