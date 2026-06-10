---
title: Mastercard chargeback reason codes (Chargeback Guide)
regulator: Mastercard
official_reference: Chargeback Guide, Merchant Edition, 19 May 2026 — Dual Message System reason codes 4853, 4837 (legacy 4841, 4860)
source_url: https://www.mastercard.com/content/dam/mccom/shared/business/support/rules-pdfs/chargeback-guide.pdf
last_verified: 2026-06-10
applies_to: disputes on Mastercard-branded cards; the issuing bank files these on the cardholder's behalf
plain_english_summary: >
  Mastercard consolidates cardholder disputes under reason code 4853 ("Cardholder Dispute"),
  with named sub-conditions including cancelled recurring transactions and refunds not processed.
  Unauthorised transactions go under 4837 ("No Cardholder Authorization") — a separate
  fraud track. The legacy codes 4841 (cancelled recurring) and 4860 (credit not processed) still
  exist but Mastercard recommends 4853. Most filings carry a 120-calendar-day issuer window.
key_clauses:
  - "4853 — Cardholder Dispute: umbrella code; eligible claims explicitly include 'Recurring transaction canceled prior to billing' and 'Refund not processed'"
  - "4853 sub-condition — Cardholder Dispute of a Recurring Transaction: merchant billed after the cardholder cancelled, or cardholder unaware of recurring terms"
  - "4853 sub-condition — Refund Not Processed: merchant agreed to or owed a refund and failed to process it"
  - "4837 — No Cardholder Authorization: cardholder did not authorise the transaction (fraud track; Single Message System equivalent: 37)"
  - "4841 — Canceled Recurring or Digital Goods Transactions: legacy, 'will eventually be eliminated', 4853 recommended"
  - "4860 — Credit Not Processed: legacy, same status, 4853 recommended"
status: verified
---

# Mastercard chargeback reason codes

**Plain-English summary — verify against the source before relying on this.**

On a Mastercard card, the cancelled-mandate-still-charged pattern files under **4853 (Cardholder Dispute)** with the recurring-transaction sub-condition; a missing refund under 4853's refund-not-processed sub-condition; a genuinely unauthorised transaction under **4837** — the fraud track. The [chargeback demand template](../../banks/hdfc/templates/03-chargeback-demand.md) uses these names in `{{NETWORK_DISPUTE_CATEGORY}}`.

## Time limits (as stated in the verified edition — these bind the issuer's filing)

- **4853 recurring-transaction dispute:** within 120 calendar days of the settlement/central-site business date.
- **4853 refund not processed:** between 15 and 120 calendar days from the refund documentation date, cancellation date, or goods-return date (immediate filing allowed on a merchant refund advice or voided receipt).
- **4837:** within 120 calendar days of the central-site business date; not usable for PIN/CDCVM-verified transactions, and capped by Mastercard's Fraud Notification Service rules after repeat fraud chargebacks on the same card number.

Banks set **shorter internal reporting windows** for cardholders than these network limits — treat the network window as the outer bound.

## The classification mirror

The guide states that 4853 *"requires that the cardholder engaged in the transaction"* — fraud claims must go via 4837. This is the same wall as Visa's 13.x/10.x split and this repo's category A vs B/C boundary ([classification.md](../../procedure/classification.md)): pick the wrong side and the filing is invalid on its face.

## Related

- [classification.md](../../procedure/classification.md) — which code fits which fact pattern
- [Visa equivalents](visa-reason-codes.md) · [RuPay](rupay-dispute-rules.md)
