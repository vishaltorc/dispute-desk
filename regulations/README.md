---
title: Regulations index
type: index
scope: every regulation entry in this repo, with what it's for in a dispute
last_verified: 2026-06-10
---

# Regulations

Plain-English **navigation summaries** of the rules that govern Indian credit card disputes — every entry links its official source and carries a `last_verified` date. **No summary here is a substitute for the source document; verify against the source before relying on anything.** Entries follow [regulation.schema.md](../schema/regulation.schema.md); anything that couldn't be confirmed on an official page is marked `UNVERIFIED`, never guessed.

## RBI

| Entry | Use it when |
|---|---|
| [rbi/recurring-payments-emandate.md](rbi/recurring-payments-emandate.md) | A recurring charge hit after mandate cancellation, or without the 24-hour pre-debit notification — the backbone of category-B disputes |
| [rbi/unauthorised-transactions-liability.md](rbi/unauthorised-transactions-liability.md) | A debit the user never authorised (category A) — liability bands tied to reporting speed, burden of proof, resolution timelines |
| [rbi/credit-card-master-direction.md](rbi/credit-card-master-direction.md) | Billing protests (30-day explanation duty), charges on disputed-as-fraud transactions, credit-bureau reporting during a dispute, the grievance machinery itself |
| [rbi/ombudsman-scheme-2021.md](rbi/ombudsman-scheme-2021.md) | **Reference only — filing is out of scope in v1.** What exists above the bank's internal ladder, and its preconditions |

## Card networks

| Entry | Use it when |
|---|---|
| [networks/visa-reason-codes.md](networks/visa-reason-codes.md) | Naming the Visa dispute category in a chargeback demand (template 03) |
| [networks/mastercard-reason-codes.md](networks/mastercard-reason-codes.md) | Same, for Mastercard cards |
| [networks/rupay-dispute-rules.md](networks/rupay-dispute-rules.md) | Same, for RuPay cards — note NPCI publishes less publicly than the international networks |

## Rules for these entries (binding on contributors and on any AI using them)

1. **Cite by linking.** Never assert what a regulation says without linking the entry, which links the source.
2. **The source wins.** A summary that disagrees with its source is a bug — fix the summary.
3. **Clause references, not full text.** These entries map documents; they do not reproduce them.
4. **Old debits, old rules.** A transaction is judged under the instrument in force on its date; entries keep predecessor/amendment tables for exactly this reason.
