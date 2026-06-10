---
title: Rejection of a non-responsive reply (deflection counter)
use_when: HDFC replied to an open complaint with something that does not address it (decision-tree S2 or S9), or you are escalating one rung with a written deflection in hand (S3, rungs below PNO).
recipient_level: same level that issued the reply (L1/L2/L3) — or one level up when used for an S3 escalation with gate G3 met
prerequisites:
  - Gate G2 — complaint reference number captured verbatim
  - The bank's reply is in hand, dated, quotable
  - The reply matches an entry in ../known-deflections.md, or its factual error is identified precisely
placeholders:
  - "{{FULL_NAME}} — cardholder name as registered"
  - "{{CARD_LAST4}} — last 4 digits of the card"
  - "{{CASE_REF}} — the bank's complaint reference number, verbatim"
  - "{{TRANSACTION_DATE}} — date of the disputed debit"
  - "{{MERCHANT_DESCRIPTOR}} — merchant as on statement"
  - "{{DISPUTED_AMOUNT}} — disputed amount in ₹"
  - "{{BANK_REPLY_DATE}} — date of the reply being rejected"
  - "{{BANK_REPLY_QUOTE}} — the operative sentence(s) of the bank's reply, quoted exactly"
  - "{{FACT_CORRECTION}} — the dated, evidenced fact that contradicts the reply (from known-deflections counter)"
  - "{{EXHIBIT_REF}} — evidence index number(s) proving the correction"
  - "{{ORIGINAL_ASK}} — the unchanged ask from the first complaint"
  - "{{RESPONSE_DEADLINE_DATE}} — the date the current rung's published SLA lapses"
attachments_expected:
  - The evidence pack as it stands (per templates-shared/evidence-index.md), including the bank's reply as a new exhibit
  - Updated timeline table with the reply and this rejection as rows
escalation_if_ignored: ../escalation-ladder.md → next rung once gate G3 is met (PNO rung uses 04-pno-escalation.md)
last_verified: 2026-06-10
---

Subject: Re: complaint {{CASE_REF}} — your reply of {{BANK_REPLY_DATE}} does not address the complaint — card ending {{CARD_LAST4}}

Dear Sir/Madam,

This concerns my open complaint {{CASE_REF}} regarding the debit of ₹{{DISPUTED_AMOUNT}} by {{MERCHANT_DESCRIPTOR}} on {{TRANSACTION_DATE}}.

Your reply dated {{BANK_REPLY_DATE}} states:

> "{{BANK_REPLY_QUOTE}}"

This does not address the complaint, for the following reason of record:

{{FACT_CORRECTION}} (see exhibit {{EXHIBIT_REF}}, attached and previously supplied).

The complaint therefore remains open and unresolved. I am not treating the reply of {{BANK_REPLY_DATE}} as a resolution, and I request that complaint {{CASE_REF}} not be marked closed on its basis. My ask is unchanged:

{{ORIGINAL_ASK}}

Please respond substantively — addressing the fact stated above — by {{RESPONSE_DEADLINE_DATE}}, the timeline published in HDFC's grievance redressal process. If the complaint is closed again without addressing it, I will escalate to the next level of that process with this correspondence attached.

Sincerely,
{{FULL_NAME}}
Card ending {{CARD_LAST4}} · Complaint {{CASE_REF}}

---

> *This draft was prepared with an organisational tool, not by a lawyer. It is not legal advice. Verify all regulatory citations against the linked primary sources and all contact details against the bank's official page before sending. No outcome is predicted or guaranteed.*
