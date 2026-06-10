---
title: Evidence index — how to assemble a numbered evidence pack
type: shared-template
used_by: every escalation from L2 upward (gate G4 makes it mandatory at L3+)
last_verified: 2026-06-10
---

# The evidence index

An escalation reviewer reads your case **cold**, often with minutes to spend. Loose screenshots make them reconstruct your story; an indexed pack makes them verify it. The difference is usually the difference between "we are looking into it" and a substantive reply. Ordering matters because the index *is* the argument: read top to bottom, it should prove the timeline without a word of commentary.

## Structure

One PDF (or one email with numbered attachments), opened by a cover sheet ([document-cover.md](document-cover.md)), then the index, then exhibits in index order.

```
EVIDENCE INDEX — complaint ref {{CASE_REF}}

E1  Statement extract showing the disputed debit       (statement, {{STATEMENT_DATE}})
E2  Proof of cancellation / mandate withdrawal          ({{CANCELLATION_PROOF_TYPE}}, {{CANCELLATION_DATE}})
E3  Pre-debit notification — or note of its absence     (notification/none, {{NOTIFICATION_DATE_OR_NONE}})
E4  Written merchant contact and reply, if any          (email, {{MERCHANT_CONTACT_DATE}})
E5  Bank complaint acknowledgement with reference no.   (email/SMS, {{L1_DATE}})
E6  Every bank reply since, in date order               (emails, dated)
E7  Timeline table                                      (templates-shared/timeline-table.md)
```

Adapt the list to the category (a category-A pack has no cancellation proof; a category-D pack opens with the two conflicting figures side by side). Keep the numbering continuous and never re-number between rungs — "E2" must mean the same document at L2 and at the PNO.

## Rules

1. **Number everything; reference by number.** The escalation email says "the mandate was cancelled on {{CANCELLATION_DATE}} (E2)" — not "see attached".
2. **One fact per exhibit.** Don't merge five screenshots into one image; the reviewer can't cite half a picture.
3. **Date every exhibit in the index line.** Undated evidence reads as unverifiable.
4. **Redact what the bank doesn't need:** full card number (keep last 4), other transactions on the statement page, third-party personal data. Never redact dates, amounts, or reference numbers in the disputed lines.
5. **Source-label each exhibit:** statement / bank email / merchant email / app screenshot. A screenshot's source and date go in its index line, since the image may not show them.
6. **The pack grows monotonically.** Each rung adds exhibits (new bank replies) at the end; nothing is removed or reordered. The PNO should be able to diff your L2 pack against your PNO pack and see only additions.
7. **Keep originals.** The pack carries extracts; the user keeps complete statements and full email threads in case they're requested.

## Privacy

The pack goes to the bank — not into this repo, not into a fork, not into a public issue. See [DISCLAIMER.md §5](../DISCLAIMER.md).
