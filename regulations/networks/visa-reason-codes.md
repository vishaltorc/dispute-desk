---
title: Visa dispute conditions (Visa Core Rules and Visa Product and Service Rules)
regulator: Visa
official_reference: Visa Core Rules and Visa Product and Service Rules, 18 April 2026 edition, Section 11 (Dispute Resolution) — conditions 11.10.3, 11.10.7, 11.10.8, 11.7.2–11.7.6
source_url: https://usa.visa.com/dam/VCOM/download/about-visa/visa-rules-public.pdf
last_verified: 2026-06-10
applies_to: disputes on Visa-branded cards; the issuing bank files these on the cardholder's behalf
plain_english_summary: >
  Visa's rulebook defines named "dispute conditions" an issuer can file. The ones this repo's
  fact patterns map to: 13.2 Cancelled Recurring Transaction, 13.6 Credit Not Processed,
  13.7 Cancelled Merchandise/Services, and the 10.x Fraud category (10.4 covers unauthorised
  card-absent transactions). Most carry a 120-calendar-day issuer filing window. A cardholder
  cannot file these directly — the issuing bank does — which is why template 03 demands
  initiation or a written refusal.
key_clauses:
  - "Dispute Condition 13.2 — Cancelled Recurring Transaction (rule 11.10.3): permission for a recurring charge was withdrawn (or account closed) before processing, but the charge was billed"
  - "Dispute Condition 13.6 — Credit Not Processed (rule 11.10.7): a credit/void receipt was issued but the credit never processed"
  - "Dispute Condition 13.7 — Cancelled Merchandise/Services (rule 11.10.8): merchandise/services cancelled or returned, still charged"
  - "Dispute Category 10 — Fraud (rules 11.7.2–11.7.6): 10.1/10.2 EMV liability shift, 10.3 other fraud card-present, 10.4 other fraud card-absent (the unauthorised-online-transaction condition), 10.5 fraud monitoring program"
status: verified
---

# Visa dispute conditions

**Plain-English summary — verify against the source before relying on this.**

When a category-B/C/D dispute on a Visa card needs the network route, the issuing bank files under a named **dispute condition**. The cancelled-mandate-still-charged pattern is condition **13.2**; a promised-but-missing refund is **13.6**; cancelled-or-returned-but-charged is **13.7**; a genuinely unauthorised card-absent transaction is category **10.4** (category A in [classification.md](../../procedure/classification.md)). The [chargeback demand template](../../banks/hdfc/templates/03-chargeback-demand.md) uses these names in `{{NETWORK_DISPUTE_CATEGORY}}`.

## Time limits (as stated in the verified edition — these bind the issuer's filing)

- **13.2:** 120 calendar days from the transaction processing date (Table 11-99).
- **13.6:** issuer must wait 15 calendar days from the date on the credit receipt, then dispute within 120 calendar days of that date (if undated, from the cancellation/return date), never beyond 540 calendar days of the transaction processing date (Table 11-125).
- **13.7:** 15-day wait from return/cancellation; 120 calendar days from processing date or from when goods/services were received/expected; 540-day outer cap (Table 11-131).
- **10.1 / 10.4:** 120 calendar days from the transaction processing date (Tables 11-11, 11-29).

Banks set **shorter internal reporting windows** for cardholders than these network limits — the network window is the outer bound, not a reason to wait.

## Two traps worth knowing (both verified in the 2026 edition)

1. **Cancellation must precede the charge for 13.2.** Effective the 18 April 2026 edition, a 13.2 dispute is invalid if the cardholder's cancellation came *after* the transaction date. The cancellation date (exhibit E2) is therefore the load-bearing fact of a category-B Visa dispute.
2. **Fraud and 13.x are mutually exclusive.** A transaction the cardholder calls fraudulent is an *invalid* 13.2/13.6 dispute — it must be filed under 10.x. This is the network-level mirror of the classification rule: category A and category B/C are different tracks, and mixing them voids both.

## Related

- [classification.md](../../procedure/classification.md) — which condition family fits which fact pattern
- [Mastercard equivalents](mastercard-reason-codes.md) · [RuPay](rupay-dispute-rules.md)
- Corroborating official source: Visa, "Dispute Management Guidelines for Visa Merchants" (June 2024), https://usa.visa.com/content/dam/VCOM/global/support-legal/documents/merchants-dispute-management-guidelines.pdf
