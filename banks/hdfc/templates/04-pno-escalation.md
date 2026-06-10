---
title: Escalation to the Principal Nodal Officer
use_when: All rungs below the PNO are exhausted — SLAs lapsed or written closures in hand — and the complaint is unresolved or wrongly closed (decision-tree S3 at the PNO rung).
recipient_level: PNO
prerequisites:
  - Gate G2 — every prior reference number captured verbatim
  - Gate G3 — the rung below has a lapsed SLA or an inadequate written outcome (quotable)
  - Gate G4 — timeline table built; evidence pack indexed and complete; ask unchanged
placeholders:
  - "{{FULL_NAME}} — cardholder name as registered"
  - "{{CARD_LAST4}} — last 4 digits of the card"
  - "{{TRANSACTION_DATE}} — date of the disputed debit"
  - "{{MERCHANT_DESCRIPTOR}} — merchant as on statement"
  - "{{DISPUTED_AMOUNT}} — disputed amount in ₹"
  - "{{DISPUTE_CATEGORY_STATEMENT}} — the same classification sentence used since the first complaint"
  - "{{ALL_CASE_REFS}} — every complaint reference issued so far, each with its filing date"
  - "{{L1_DATE}} — date the first complaint was filed"
  - "{{TOTAL_DAYS_PENDING}} — days from first complaint to this email"
  - "{{ESCALATION_HISTORY}} — 3–6 numbered lines: rung, date, reference, outcome quoted in half a sentence"
  - "{{ONE_SENTENCE_ASK}} — the single specific ask, unchanged from the first complaint"
  - "{{RESPONSE_DEADLINE_DATE}} — date the PNO-level published SLA lapses (from contacts.md sla_days)"
attachments_expected:
  - Full evidence pack with cover sheet (templates-shared/document-cover.md), index, and all exhibits
  - Complete timeline table — every event from first cancellation/transaction to this escalation
escalation_if_ignored: ../escalation-ladder.md rung 5 — internal ladder exhausted (gate G5); this repo's guidance stops there (see procedure/preconditions.md G5)
last_verified: 2026-06-10
---

Subject: Escalation to Principal Nodal Officer — unresolved complaint(s) {{ALL_CASE_REFS}} — card ending {{CARD_LAST4}} — pending {{TOTAL_DAYS_PENDING}} days

Dear Principal Nodal Officer,

I am escalating an unresolved credit card dispute to you as HDFC Bank's Principal Nodal Officer, having exhausted the levels below in HDFC's published grievance redressal process.

**The dispute.** {{DISPUTE_CATEGORY_STATEMENT}} The debit: ₹{{DISPUTED_AMOUNT}} by {{MERCHANT_DESCRIPTOR}} on {{TRANSACTION_DATE}}, on my credit card ending {{CARD_LAST4}}.

**The history.** First complaint filed {{L1_DATE}}; pending {{TOTAL_DAYS_PENDING}} days as of this email. References and outcomes:

{{ESCALATION_HISTORY}}

The full chronology is in the attached timeline table; every statement in it is supported by a numbered exhibit in the attached, indexed evidence pack. My classification and my ask have not changed at any level.

**The ask.** {{ONE_SENTENCE_ASK}}

I request your written response by {{RESPONSE_DEADLINE_DATE}}, per the timeline HDFC publishes for this level. If the complaint remains unresolved or is again closed without addressing the facts of record, I will pursue the remedies available beyond the bank's internal process.

Sincerely,
{{FULL_NAME}}
Card ending {{CARD_LAST4}} · References: {{ALL_CASE_REFS}}

---

> *This draft was prepared with an organisational tool, not by a lawyer. It is not legal advice. Verify all regulatory citations against the linked primary sources and all contact details against the bank's official page before sending. No outcome is predicted or guaranteed.*
