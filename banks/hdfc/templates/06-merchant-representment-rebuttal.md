---
title: Rebuttal of merchant representment
use_when: A chargeback was raised, the merchant responded (representment / second presentment), and HDFC has re-applied the charge or signalled it will accept the merchant's response (decision-tree S5).
recipient_level: the rung handling the chargeback (typically L2/L3 — see banks/hdfc/escalation-ladder.md)
prerequisites:
  - Gate G2 — complaint and chargeback references captured
  - Gate G3 — the representment outcome is in writing from the bank
  - A copy of the merchant's representment documents has been requested (demand it in this email if the bank has not supplied it)
placeholders:
  - "{{FULL_NAME}} — cardholder name as registered"
  - "{{CARD_LAST4}} — last 4 digits of the card"
  - "{{CASE_REF}} — complaint reference, verbatim"
  - "{{CHARGEBACK_REF}} — chargeback/dispute reference if the bank issued one, else 'not provided'"
  - "{{TRANSACTION_DATE}} — date of the disputed debit"
  - "{{MERCHANT_DESCRIPTOR}} — merchant as on statement"
  - "{{DISPUTED_AMOUNT}} — disputed amount in ₹"
  - "{{REPRESENTMENT_DATE}} — date the bank communicated the merchant's response / re-applied the charge"
  - "{{MERCHANT_CLAIM_SUMMARY}} — what the merchant is claimed to have shown, as the bank stated it (quote where possible)"
  - "{{REBUTTAL_POINTS}} — numbered points, each pairing one merchant claim with one dated, exhibited fact that answers it"
  - "{{ONE_SENTENCE_ASK}} — typically: re-present the dispute / proceed to the next dispute stage with the rebuttal evidence"
  - "{{RESPONSE_DEADLINE_DATE}} — date the current rung's published SLA lapses"
attachments_expected:
  - Evidence pack updated with the bank's representment communication and every exhibit cited in {{REBUTTAL_POINTS}}
  - Updated timeline table
escalation_if_ignored: next rung per ../escalation-ladder.md (04-pno-escalation.md at the PNO rung), with this rebuttal attached
last_verified: 2026-06-10
---

Subject: Complaint {{CASE_REF}} / chargeback {{CHARGEBACK_REF}} — rebuttal of merchant representment of {{REPRESENTMENT_DATE}} — card ending {{CARD_LAST4}}

Dear Sir/Madam,

This concerns the chargeback raised on complaint {{CASE_REF}} for the debit of ₹{{DISPUTED_AMOUNT}} by {{MERCHANT_DESCRIPTOR}} on {{TRANSACTION_DATE}} (card ending {{CARD_LAST4}}).

On {{REPRESENTMENT_DATE}} I was informed that the merchant has responded and that the charge stands or will be re-applied, on the following basis:

{{MERCHANT_CLAIM_SUMMARY}}

If a copy of the merchant's representment documents has not already been provided to me, I request it now — I am entitled to know what is being relied on against my dispute. On the basis communicated so far, the merchant's response does not answer the facts of record:

{{REBUTTAL_POINTS}}

Each point above cites a numbered exhibit in the attached, indexed evidence pack; none of this evidence is new — it has been on record with HDFC since the dates shown in the attached timeline table.

**The ask.** {{ONE_SENTENCE_ASK}}

Please confirm in writing, by {{RESPONSE_DEADLINE_DATE}}: (1) that this rebuttal and its exhibits have been taken into the dispute record, and (2) the next stage of the network dispute process that HDFC will pursue, or — if HDFC declines to proceed — the specific reason, in writing.

Sincerely,
{{FULL_NAME}}
Card ending {{CARD_LAST4}} · Complaint {{CASE_REF}}

---

> *This draft was prepared with an organisational tool, not by a lawyer. It is not legal advice. Verify all regulatory citations against the linked primary sources and all contact details against the bank's official page before sending. No outcome is predicted or guaranteed.*
