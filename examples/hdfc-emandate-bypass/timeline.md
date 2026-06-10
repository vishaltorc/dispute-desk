---
title: Worked example — timeline table (synthetic)
type: example
status: fully synthetic — all dates, references, and amounts invented for illustration
illustrates: templates-shared/timeline-table.md applied to the narrative in narrative.md
last_verified: 2026-06-10
---

# Timeline table — as it stood at the L2 escalation

> Synthetic illustration of the [timeline-table format](../../templates-shared/timeline-table.md). Note the rows for *non-events* (missing pre-debit notification, lapsed SLA) — absence of a required act is an event. Exhibit numbers refer to the [evidence-index structure](../../templates-shared/evidence-index.md); the synthetic pack is described, not included (no real documents exist).

| date | event | reference | source |
|---|---|---|---|
| 2026-01-05 | E-mandate for STREAMCO cancelled via HDFC card-controls app; in-app confirmation received | MNDT-0001 | E2 |
| 2026-02-01 | Debit of ₹1,499 by STREAMCO MUMBAI processed to card ending 4321 | — | E1 |
| 2026-02-01 | No pre-debit notification received before this debit (required ≥24h prior) | — | E3 (absence noted) |
| 2026-02-02 | Written complaint to STREAMCO support; reply: billing "handled by payment partner" | SC-TKT-9 | E4 |
| 2026-02-04 | Dispute filed with HDFC (template 01, category B); reference issued | CC-0000001 | E5 |
| 2026-02-18 | Bank reply #1: "please cancel the mandate with the merchant" (deflection D1) | CC-0000001 | E6.1 |
| 2026-02-19 | Rejection sent (template 02): cancellation of 2026-01-05 re-evidenced; basis of post-withdrawal debit queried | CC-0000001 | E6.2 |
| 2026-02-27 | Bank reply #2: "no debit was processed on the mandate, as it stands cancelled" (deflections D2/D3) | CC-0000001 | E6.3 |
| 2026-02-28 | Counter sent: statement line cited (E1); e-mandate framework cited via repo entry; merchant card-on-file bypass named | CC-0000001 | E6.4 |
| 2026-02-28 | Formal chargeback demand sent (template 03): cancelled-recurring network category named, window noted | CC-0000001 | E6.5 |
| 2026-03-14 | L1 SLA on the 2026-02-28 counters lapsed with no substantive reply | CC-0000001 | timeline arithmetic |
| 2026-03-16 | L2 escalation sent with cover sheet, this table, and indexed pack E1–E6 (gates G2/G3/G4 checked) | CC-0000001 | E7 |

## What this table is doing (format notes)

1. **Every row is sourced** — to an exhibit, a reference, or explicit arithmetic. No row relies on recollection.
2. **The bank's own words appear as dated rows**, quoted in half-sentences — the two deflections are the two sharpest rows in the table.
3. **Append-only:** rows 1–10 were identical in every email from 2026-02-28 onward; later rungs only ever saw additions.
4. **The non-event rows** (missing notification, lapsed SLA) are what convert "they ignored me" into a record.
