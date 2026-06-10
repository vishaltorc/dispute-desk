---
title: Regulation entry schema
type: schema
defines: required fields for every file under regulations/
last_verified: 2026-06-10
---

# regulation.schema — required fields for a regulation entry

A regulation entry is a **pointer with a map**, not a copy of the law. It exists so an AI can (a) find the right official document fast, (b) cite it by clause, and (c) never assert regulatory content without a link. The plain-English summary is for navigation only.

## Front-matter fields (all required)

| Field | Format | Rule |
|---|---|---|
| `title` | official document title | As the regulator publishes it. |
| `regulator` | `RBI` / `Visa` / `Mastercard` / `RuPay (NPCI)` | Who issued it. |
| `official_reference` | circular/direction/rule number | Exactly as printed on the document. `UNVERIFIED` if it could not be confirmed on an official page. |
| `source_url` | official-domain URL | rbi.org.in, visa.com, mastercard.com/.us, npci.org.in only. The page or PDF the entry was verified against. |
| `last_verified` | `YYYY-MM-DD` | Date `source_url` was actually loaded and checked. |
| `applies_to` | one line | e.g. "recurring card transactions on Indian-issued cards". |
| `plain_english_summary` | 2–4 sentences | Navigation summary. The body must label it (see below). |
| `key_clauses` | list | `clause ref — one-line description`, one per clause that matters for disputes. |
| `status` | `verified` / `UNVERIFIED` | Whether `official_reference` + clauses were confirmed against `source_url`. |

## Body rules

1. The body opens with this bold line, verbatim, immediately after the heading:
   **Plain-English summary — verify against the source before relying on this.**
2. **No full-text reproduction.** Clause references and one-line descriptions only. Link the official document; the reader reads the law there. (Short phrases needed to identify a clause are fine; paragraphs are not.)
3. **No advice framing.** Entries describe what a rule covers and where it lives — they do not tell a user what they are entitled to in their specific case, and they never predict outcomes.
4. **Unverified means flagged.** If any number, date, or clause could not be confirmed on the official source, mark it `UNVERIFIED` inline and in `status`, with a note on what was checked. A wrong-but-confident citation is the single most damaging error this repo can ship — it hands the bank a reason to dismiss the complaint.
5. **Amendments tracked in place.** If a circular was amended (e.g. limits raised), the entry lists each amendment with its own `official_reference` + `source_url` + date, newest clearly marked as current.

## Skeleton

```markdown
---
title:
regulator:
official_reference:
source_url:
last_verified:
applies_to:
plain_english_summary: >
  …
key_clauses:
  - "clause ref — one-line description"
status: verified
---

# <title>

**Plain-English summary — verify against the source before relying on this.**

<the 2–4 sentence summary, expanded only as far as navigation requires>

## Key clauses
…

## Amendments (if any)
…
```
