---
title: Timeline table — the chronological backbone of any complaint
type: shared-template
used_by: every escalation; exhibit E-last in the evidence pack; pasted inline at L2+
last_verified: 2026-06-10
---

# The timeline table

A dispute is a story about dates: what happened, when, who was told, and who failed to act within what window. The timeline table compresses that story into something a reviewer can verify in thirty seconds. It is the strongest single artifact in an escalation because it converts a complaint ("they ignored me") into a record ("filed {{DATE}}, ref {{REF}}, SLA lapsed {{DATE}}").

## Format

Four columns, strict chronological order, one row per event:

| date | event | reference | source |
|---|---|---|---|
| `YYYY-MM-DD` | one factual sentence | ticket/email ref or `—` | exhibit number (E1…) or channel |

## Synthetic example (illustrative only — every value below is fake)

| date | event | reference | source |
|---|---|---|---|
| 2026-01-05 | E-mandate for {{MERCHANT}} cancelled via bank app; confirmation received | MNDT-XXXX | E2 |
| 2026-02-03 | Debit of ₹{{AMOUNT}} by same merchant appears on statement | — | E1 |
| 2026-02-03 | No pre-debit notification received for this debit | — | E3 |
| 2026-02-04 | Dispute filed with bank phone banking; reference issued | CC-XXXXXXX | E5 |
| 2026-02-18 | Bank reply: "cancel the mandate with the merchant" — mandate already cancelled 2026-01-05 | CC-XXXXXXX | E6 |
| 2026-02-19 | Deflection rejected in writing; cancellation proof re-attached | CC-XXXXXXX | E6 |

## Rules

1. **Facts only, no adjectives.** "Bank reply did not address the cancellation" is a fact; "bank fobbed me off" is not. The table argues by sequence, not by tone.
2. **Every row sourced.** A row that no exhibit or reference supports gets cut — one unsupported row taints the table.
3. **Include the bank's actions, verbatim where short.** Quoted half-sentences from bank replies (with their date and reference) are the table's sharpest rows.
4. **Include non-events when an obligation existed.** "No pre-debit notification received" or "SLA of {{N}} days lapsed with no response" are rows — absence of a required act is an event.
5. **Never backfill from memory.** A date the user can't evidence goes in as approximate and marked (`~2026-01-xx, per user recollection`) or is left out. A provably-wrong date hands the bank the whole table.
6. **One table, append-only.** Same table at every rung, new rows added at the bottom as events occur — identical history every time it's seen.
