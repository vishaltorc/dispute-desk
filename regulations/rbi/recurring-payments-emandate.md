---
title: Digital Payments – E-mandate Framework, 2026 (and predecessor e-mandate circulars)
regulator: RBI
official_reference: RBI/DPSS/2026-27/396; RBI/CO.DPSS.POLC.No.S56/02.14.003/2026-27 (both reference strings appear on the official page)
source_url: https://www.rbi.org.in/Scripts/BS_ViewMasDirections.aspx?id=13374
last_verified: 2026-06-10
applies_to: recurring transactions under e-mandates on Indian-issued cards (and other digital payment instruments), including subscription and standing-instruction debits
plain_english_summary: >
  Recurring card debits in India must run inside RBI's e-mandate framework: the mandate is
  registered with additional-factor authentication (AFA), the issuer must notify the customer at
  least 24 hours before each debit, and the customer can opt out of a single debit or withdraw the
  whole mandate at any time — after which further recurring debits must not be processed. Debits
  above the AFA-exemption limit require fresh authentication. RBI's limited-liability rules for
  unauthorised transactions expressly apply to e-mandate debits.
key_clauses:
  - "Clause 4(a) — one-time mandate registration requires AFA validation"
  - "Clause 4(b) — mandate must state a validity period; issuer must provide a facility to modify or withdraw the mandate at any time"
  - "Clause 4(e) — modification or withdrawal of a mandate requires AFA validation"
  - "Clause 6(a) — pre-transaction notification at least 24 hours before the actual charge/debit"
  - "Clause 6(b) — notification must state: merchant name, amount, date/time of debit, e-mandate reference number, reason for debit"
  - "Clause 6(c) — customer may opt out of a particular transaction or the entire e-mandate on receiving the notification; issuer must act on it (AFA-validated) and confirm"
  - "Clause 6(d) — carve-out: pre-debit notification not required for FASTag/NCMC auto-replenishment mandates"
  - "Clause 7 — post-transaction notification with the same particulars plus grievance redressal details"
  - "Clause 8(a) — AFA-exemption limit ₹15,000 per transaction (general); above it, AFA required"
  - "Clause 8(b) — ₹1,00,000 per transaction limit for insurance premia, mutual fund subscriptions, and credit card bill payments"
  - "Clause 9(a) — issuer must have a dispute/grievance redressal system for e-mandate transactions"
  - "Clause 9(b) — RBI's limited-liability instructions for unauthorised electronic transactions apply to e-mandate recurring transactions"
  - "Clause 10(a) — no charges to the customer for the e-mandate facility"
  - "Clause 11 — repeals the predecessor circulars listed below"
status: verified
---

# RBI e-mandate framework for recurring transactions

**Plain-English summary — verify against the source before relying on this.**

If a merchant debits an Indian-issued card on a recurring basis, that debit is supposed to live inside RBI's e-mandate framework: AFA-validated registration, a pre-debit notification at least 24 hours before each charge (stating merchant, amount, date, reference, and reason), an opt-out on every notification, and an always-available facility to withdraw the mandate — after which further recurring debits must not be processed. The framework also instructs that RBI's limited-liability rules for unauthorised transactions apply to these debits (see [unauthorised-transactions-liability.md](unauthorised-transactions-liability.md)).

Why this matters in a dispute: a recurring debit that arrives **after a mandate withdrawal**, or **without the required pre-debit notification**, is a debit processed outside the framework's conditions — which is the factual basis of a category-B complaint ([classification](../../procedure/classification.md)) and of deflection counters D1/D3 ([known-deflections](../../banks/hdfc/known-deflections.md)).

## Key clauses

See `key_clauses` in the front-matter above; the dispute-critical ones are 4(b)/4(e) (withdrawal right), 6(a)–(c) (pre-debit notification and opt-out), and 9(b) (limited-liability rules apply).

## Predecessor circulars (repealed by clause 11, but governing debits processed while in force)

A debit is judged under the instrument in force on its date. All verified on rbi.org.in, 2026-06-10:

| Instrument | Reference | Date | Source | Dispute-relevant content |
|---|---|---|---|---|
| Processing of e-mandate on cards for recurring transactions | RBI/2019-20/47, DPSS.CO.PD.No.447/02.14.003/2019-20 | 2019-08-21 (effective 2019-09-01) | [rbi.org.in Id=11668](https://www.rbi.org.in/Scripts/NotificationUser.aspx?Id=11668) | The original framework: AFA registration (Annex ¶2), 24-hour pre-debit notification (¶8–9), opt-out (¶10), online withdrawal facility + no debits after withdrawal (¶15–16), merchant must delete card details on withdrawal (¶17), grievance/dispute handling (¶18–19), limited-liability rules apply (¶20). AFA limit ₹2,000 (¶4). |
| UPI extension | RBI/2019-20/139, DPSS.CO.PD No.1324/02.23.001/2019-20 | 2020-01-10 | [Id=11784](https://www.rbi.org.in/Scripts/NotificationUser.aspx?Id=11784) | Extends the framework to UPI, mutatis mutandis. |
| Limit raised to ₹5,000 | RBI/2020-21/74, DPSS.CO.PD No.754/02.14.003/2020-21 | 2020-12-04 (effective 2021-01-01) | [Id=12002](https://www.rbi.org.in/Scripts/NotificationUser.aspx?Id=12002) | Also: non-compliant recurring arrangements "shall not be continued beyond March 31, 2021" (¶3). |
| Compliance deadline extension | RBI/2020-21/118, CO.DPSS.POLC.No.S34/02-14-003/2020-2021 | 2021-03-31 | [Id=12051](https://www.rbi.org.in/Scripts/NotificationUser.aspx?Id=12051) | Final extension to 2021-09-30; no new non-compliant mandates during extension. |
| Limit raised to ₹15,000 | RBI/2022-23/73, CO.DPSS.POLC.No.S-518/02.14.003/2022-23 | 2022-06-16 | [Id=12341](https://www.rbi.org.in/Scripts/NotificationUser.aspx?Id=12341) | AFA-exemption limit ₹5,000 → ₹15,000. |
| ₹1,00,000 for three categories | RBI/2023-2024/88, CO.DPSS.POLC.No.S-882/02.14.003/2023-24 | 2023-12-12 | [Id=12570](https://www.rbi.org.in/Scripts/NotificationUser.aspx?Id=12570) | Higher limit only for mutual funds, insurance premia, credit card bill payments. |
| FASTag/NCMC auto-replenishment | RBI/2024-25/64, CO.DPSS.POLC.No.S528/02-14-003/2024-25 | 2024-08-22 | [Id=12722](https://www.rbi.org.in/Scripts/NotificationUser.aspx?Id=12722) | Brings auto-replenishment under the framework; exempts it from the 24-hour pre-debit notification. |

Also repealed: a "Clarification issued to IBA on e-mandate based recurring transactions" dated 2021-10-08, named in the 2026 framework's repeal table without a circular number. Its standalone URL: `UNVERIFIED` — it appears to have been a clarification letter to the Indian Banks' Association, not a numbered public circular; it is cited here only as listed in the repeal table.

## Related

- The credit-card Master Direction's billing-dispute clauses: [credit-card-master-direction.md](credit-card-master-direction.md)
- Liability when a debit is treated as unauthorised: [unauthorised-transactions-liability.md](unauthorised-transactions-liability.md)
- The network dispute category for cancelled recurring charges: [Visa](../networks/visa-reason-codes.md) · [Mastercard](../networks/mastercard-reason-codes.md) · [RuPay](../networks/rupay-dispute-rules.md)
