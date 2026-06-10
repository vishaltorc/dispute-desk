---
title: Amount correction — partial or incorrect credit
use_when: HDFC has resolved the dispute in principle but the credited amount is wrong — partial refund, or disputed-charge late fees, interest, or GST on fees not reversed (decision-tree S6).
recipient_level: the rung that issued the credit (L1/L2/L3)
prerequisites:
  - Gate G2 — complaint reference captured
  - The credit has actually posted (statement line in hand), so the delta is computable from documents, not estimates
placeholders:
  - "{{FULL_NAME}} — cardholder name as registered"
  - "{{CARD_LAST4}} — last 4 digits of the card"
  - "{{CASE_REF}} — complaint reference, verbatim"
  - "{{TRANSACTION_DATE}} — date of the original disputed debit"
  - "{{MERCHANT_DESCRIPTOR}} — merchant as on statement"
  - "{{DISPUTED_AMOUNT}} — the amount disputed and upheld"
  - "{{CREDIT_DATE}} — date the credit posted"
  - "{{CREDITED_AMOUNT}} — the amount actually credited, exactly as on the statement"
  - "{{ITEMISATION}} — table rows: each missing component (principal shortfall / late fee dated X / interest for cycle Y / GST on fee Z), its amount, and the statement line evidencing it"
  - "{{DELTA_AMOUNT}} — the total still owed: sum of the itemisation"
  - "{{EXHIBIT_REF}} — evidence index number(s) for the statement lines cited"
  - "{{RESPONSE_DEADLINE_DATE}} — date the current rung's published SLA lapses"
attachments_expected:
  - Statement extracts showing the original debit, the credit, and every fee/interest line in the itemisation
  - Updated timeline table
escalation_if_ignored: 02-reject-deflection.md at the next rung per ../escalation-ladder.md, with the itemisation unchanged
last_verified: 2026-06-10
---

Subject: Complaint {{CASE_REF}} — credited amount incorrect — ₹{{DELTA_AMOUNT}} outstanding — card ending {{CARD_LAST4}}

Dear Sir/Madam,

Thank you for the credit of ₹{{CREDITED_AMOUNT}} posted on {{CREDIT_DATE}} against complaint {{CASE_REF}} (debit of ₹{{DISPUTED_AMOUNT}} by {{MERCHANT_DESCRIPTOR}} on {{TRANSACTION_DATE}}, card ending {{CARD_LAST4}}).

The credit does not fully reverse the impact of the disputed debit. The components still outstanding, each evidenced by a statement line (exhibit {{EXHIBIT_REF}}):

{{ITEMISATION}}

**Total outstanding: ₹{{DELTA_AMOUNT}}.**

Since these fees, interest, and tax arose solely from the disputed debit that has now been credited, I request that they be reversed in full, and that the reversal be reflected with appropriate value-dating so that no further interest accrues on them.

Please confirm in writing by {{RESPONSE_DEADLINE_DATE}}: (1) the reversal of each itemised component, or (2) for any component HDFC declines to reverse, the specific written reason, line by line.

Complaint {{CASE_REF}} should remain open until this reconciliation is complete.

Sincerely,
{{FULL_NAME}}
Card ending {{CARD_LAST4}} · Complaint {{CASE_REF}}

---

> *This draft was prepared with an organisational tool, not by a lawyer. It is not legal advice. Verify all regulatory citations against the linked primary sources and all contact details against the bank's official page before sending. No outcome is predicted or guaranteed.*
