---
title: Bank folder schema
type: schema
defines: required structure for any banks/<bank>/ folder
last_verified: 2026-06-10
---

# bank.schema — required structure for a bank folder

Every folder under `banks/` must be **self-contained**: an AI assistant given only `procedure/`, `regulations/`, `templates-shared/`, and one bank folder must be able to run a full dispute for that bank. `banks/hdfc/` is the reference implementation — copy it to start a new bank.

## Folder name

Lowercase, hyphenated, recognisable: `hdfc`, `icici`, `axis`, `sbi-card`.

## Required files

| File | Purpose | Schema it must follow |
|---|---|---|
| `README.md` | Bank overview: which products are covered, quirks (e.g. multiple email domains), folder map | front-matter: `title`, `bank`, `products_covered`, `last_verified` |
| `contacts.md` | Every escalation contact, dated and source-linked | [contact.schema.md](contact.schema.md) per entry |
| `escalation-ladder.md` | The bank's specific rung-by-rung ladder, each rung referencing `contacts.md` and a template | front-matter: `title`, `bank`, `levels` (ordered list), `last_verified` |
| `known-deflections.md` | Documented stall patterns + factual counters, each linked to a template | front-matter: `title`, `bank`, `entries` (count); per entry: `deflection`, `why_incomplete`, `correct_response`, `template` |
| `templates/` | Numbered templates, `NN-purpose.md`, ordered by typical escalation sequence | each file follows [template.schema.md](template.schema.md) |

## Rules

- **Numbering:** templates are `01-…` through `NN-…` in rough escalation order, so an AI can infer sequence from filenames alone.
- **No bank-agnostic logic here.** Universal procedure (category classification, precondition logic, the abstract ladder) lives in `procedure/`. A bank folder holds only what is specific to that bank: contacts, its concrete ladder, its observed deflections, its addressed templates.
- **Self-containment over DRY:** it is acceptable for a bank's escalation-ladder to restate rung descriptions that resemble the universal ladder — an AI may load only the bank folder plus `procedure/`, and a contributor copying the folder needs the full picture in place.
- **Everything dated:** any factual claim about the bank (an SLA, a contact, a portal URL) carries `last_verified` and `source_url` exactly as [contact.schema.md](contact.schema.md) requires.

## Copy-paste starting point

```
banks/<bank>/
├── README.md
├── contacts.md            # re-source every entry from <bank>'s official pages
├── escalation-ladder.md   # rebuild from <bank>'s published grievance levels
├── known-deflections.md   # start empty-ish; grow from documented cases
└── templates/
    ├── 01-initial-dispute.md
    ├── 02-reject-deflection.md
    ├── 03-chargeback-demand.md
    ├── 04-pno-escalation.md
    ├── 05-grievance-officer.md
    ├── 06-merchant-representment-rebuttal.md
    └── 07-amount-correction.md
```
