---
title: INDEX — intent → file lookup
type: index
note: generated at build time; update when files are added or moved (CONTRIBUTING.md checklist)
last_verified: 2026-06-10
---

# INDEX

One-hop lookup from what you (or the user) need to the file that has it. AI assistants: read [HOW_AI_SHOULD_USE_THIS.md](HOW_AI_SHOULD_USE_THIS.md) before using anything below.

## Start here

| Intent | File |
|---|---|
| Understand what this repo is and its limits | [README.md](README.md) |
| The disclaimer that applies to everything | [DISCLAIMER.md](DISCLAIMER.md) |
| Operating instructions for an AI assistant | [HOW_AI_SHOULD_USE_THIS.md](HOW_AI_SHOULD_USE_THIS.md) |
| Add a bank / contribute | [CONTRIBUTING.md](CONTRIBUTING.md) |

## "Help me with my dispute" (procedure)

| Intent | File |
|---|---|
| Find the user's current state and the single correct next step | [procedure/decision-tree.md](procedure/decision-tree.md) |
| Check whether a step is allowed yet (gates G0–G5) | [procedure/preconditions.md](procedure/preconditions.md) |
| Pick the correct dispute category (this decides everything) | [procedure/classification.md](procedure/classification.md) |
| Understand the escalation order and why skipping rungs fails | [procedure/escalation-ladder.md](procedure/escalation-ladder.md) |

## HDFC specifics

| Intent | File |
|---|---|
| Who to write to, with freshness dates and sources | [banks/hdfc/contacts.md](banks/hdfc/contacts.md) |
| HDFC's actual rung order, SLAs, and which template per rung | [banks/hdfc/escalation-ladder.md](banks/hdfc/escalation-ladder.md) |
| The bank replied with a non-answer — match and counter it | [banks/hdfc/known-deflections.md](banks/hdfc/known-deflections.md) |
| HDFC quirks (domain migration, parallel desks) | [banks/hdfc/README.md](banks/hdfc/README.md) |

## Drafting (HDFC templates)

| Situation (decision-tree state) | Template |
|---|---|
| First complaint, any category (S0) | [01-initial-dispute](banks/hdfc/templates/01-initial-dispute.md) |
| Reply doesn't address the complaint (S2, S9) | [02-reject-deflection](banks/hdfc/templates/02-reject-deflection.md) |
| Bank won't raise the network dispute / window closing (S4) | [03-chargeback-demand](banks/hdfc/templates/03-chargeback-demand.md) |
| Escalate to the PNO — Rung 3 (S3) | [04-pno-escalation](banks/hdfc/templates/04-pno-escalation.md) |
| Escalate to the Grievance Redressal Officer — Rung 2 (S3) | [05-grievance-officer](banks/hdfc/templates/05-grievance-officer.md) |
| Merchant's representment accepted (S5) | [06-merchant-representment-rebuttal](banks/hdfc/templates/06-merchant-representment-rebuttal.md) |
| Credit posted but the amount is wrong (S6) | [07-amount-correction](banks/hdfc/templates/07-amount-correction.md) |

## Evidence formats (any bank)

| Intent | File |
|---|---|
| Assemble the numbered evidence pack | [templates-shared/evidence-index.md](templates-shared/evidence-index.md) |
| Build the chronological timeline table | [templates-shared/timeline-table.md](templates-shared/timeline-table.md) |
| Cover sheet for a PDF submission | [templates-shared/document-cover.md](templates-shared/document-cover.md) |

## Regulations (all source-linked; summaries are navigation only)

| Intent | File |
|---|---|
| Regulation index with "use when" guidance | [regulations/README.md](regulations/README.md) |
| Recurring charge after cancellation / missing pre-debit notice | [regulations/rbi/recurring-payments-emandate.md](regulations/rbi/recurring-payments-emandate.md) |
| Unauthorised transaction — liability bands, burden of proof | [regulations/rbi/unauthorised-transactions-liability.md](regulations/rbi/unauthorised-transactions-liability.md) |
| Billing protests, disputed-charge fees, bureau reporting, grievance machinery | [regulations/rbi/credit-card-master-direction.md](regulations/rbi/credit-card-master-direction.md) |
| What exists above the bank (reference only; filing out of scope) | [regulations/rbi/ombudsman-scheme-2021.md](regulations/rbi/ombudsman-scheme-2021.md) |
| Visa dispute condition to cite | [regulations/networks/visa-reason-codes.md](regulations/networks/visa-reason-codes.md) |
| Mastercard reason code to cite | [regulations/networks/mastercard-reason-codes.md](regulations/networks/mastercard-reason-codes.md) |
| RuPay — what is (and isn't) publicly citable | [regulations/networks/rupay-dispute-rules.md](regulations/networks/rupay-dispute-rules.md) |

## Worked example (synthetic, illustrative only)

| Intent | File |
|---|---|
| See the whole flow on one fact pattern | [examples/hdfc-emandate-bypass/narrative.md](examples/hdfc-emandate-bypass/narrative.md) |
| See the timeline-table format in use | [examples/hdfc-emandate-bypass/timeline.md](examples/hdfc-emandate-bypass/timeline.md) |
| The transferable mechanics, minus the one-off facts | [examples/hdfc-emandate-bypass/what-worked.md](examples/hdfc-emandate-bypass/what-worked.md) |

## Schemas (for contributors and validators)

| Intent | File |
|---|---|
| Required structure of a bank folder | [schema/bank.schema.md](schema/bank.schema.md) |
| Required fields of a contact entry | [schema/contact.schema.md](schema/contact.schema.md) |
| Required front-matter of a template | [schema/template.schema.md](schema/template.schema.md) |
| Required fields of a regulation entry | [schema/regulation.schema.md](schema/regulation.schema.md) |
