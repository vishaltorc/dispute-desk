---
title: Initial dispute — credit card transaction
use_when: First formal complaint to HDFC about a disputed credit card transaction (decision-tree S0, any category). Nothing has been filed yet.
recipient_level: L1
prerequisites:
  - Gate G0 — all facts captured (statement line, card last-4, prior contact history)
  - Gate G1 — dispute classified per procedure/classification.md and stated to the user
  - Category C only — one written merchant attempt exists, or a stated reason it would be futile
placeholders:
  - "{{FULL_NAME}} — cardholder name as registered with HDFC"
  - "{{CARD_LAST4}} — last 4 digits of the credit card (never the full number)"
  - "{{REGISTERED_MOBILE}} — mobile registered with the bank"
  - "{{TRANSACTION_DATE}} — date of the disputed debit, exactly as on the statement"
  - "{{MERCHANT_DESCRIPTOR}} — merchant name exactly as printed on the statement"
  - "{{DISPUTED_AMOUNT}} — amount in ₹, exactly as on the statement"
  - "{{DISPUTE_CATEGORY_STATEMENT}} — the one-sentence classification from procedure/classification.md"
  - "{{DISPUTE_REASON_ONE_LINE}} — what happened, in the user's words, one sentence"
  - "{{CATEGORY_PARAGRAPH}} — the category-specific paragraph (see body comments)"
  - "{{CANCELLATION_DATE}} — (conditional, category B) date the mandate/consent was cancelled"
  - "{{CANCELLATION_METHOD}} — (conditional, category B) how it was cancelled (app/merchant portal/email)"
  - "{{MERCHANT_CONTACT_DATE}} — (conditional, category C) date of the written merchant attempt"
  - "{{EVIDENCE_LIST}} — numbered list of attachments per templates-shared/evidence-index.md"
attachments_expected:
  - Statement extract showing the disputed line (E1)
  - Category B — proof of cancellation / note of missing pre-debit notification (E2/E3)
  - Category C — written merchant contact and any reply (E4)
escalation_if_ignored: ../escalation-ladder.md → L2 via 02-reject-deflection.md once gate G3 is met
last_verified: 2026-06-10
---

Subject: Dispute of credit card transaction — card ending {{CARD_LAST4}} — ₹{{DISPUTED_AMOUNT}} on {{TRANSACTION_DATE}} — request for dispute registration and reference number

Dear Sir/Madam,

I am disputing the following transaction on my HDFC Bank credit card ending {{CARD_LAST4}} (registered mobile {{REGISTERED_MOBILE}}):

- Date: {{TRANSACTION_DATE}}
- Merchant (as on statement): {{MERCHANT_DESCRIPTOR}}
- Amount: ₹{{DISPUTED_AMOUNT}}

{{DISPUTE_CATEGORY_STATEMENT}} {{DISPUTE_REASON_ONE_LINE}}

{{CATEGORY_PARAGRAPH}}

<!-- AI: build {{CATEGORY_PARAGRAPH}} from exactly one of the following, filled from user facts.
  Category A: "I did not make or authorise this transaction. I am reporting it as an unauthorised
  electronic transaction within the meaning of the RBI's customer-protection framework
  (see regulations/rbi/unauthorised-transactions-liability.md — cite the circular by its verified
  reference, with link), and I request that my reporting date today be recorded, given that the
  framework ties customer liability to the speed of reporting."
  Category B: "I cancelled the e-mandate / recurring consent for this merchant on
  {{CANCELLATION_DATE}} via {{CANCELLATION_METHOD}} (proof attached). The debit above was processed
  after that cancellation [and without the pre-debit notification required under the RBI e-mandate
  framework — include only if true]. I request that this dispute be handled under that framework
  (see regulations/rbi/recurring-payments-emandate.md — cite by verified reference, with link)."
  -- If used, add {{CANCELLATION_DATE}} and {{CANCELLATION_METHOD}} to the interview.
  Category C: "I authorised this transaction but the service/goods were not provided as agreed
  [one line of specifics]. I contacted the merchant in writing on {{MERCHANT_CONTACT_DATE}}
  (copy attached) and [no resolution / no reply] resulted."
  -- If used, add {{MERCHANT_CONTACT_DATE}} to the interview.
  Category D: "This is a processing error: [duplicate charge / incorrect amount — state the agreed
  figure vs the charged figure, both exactly as evidenced]."
-->

I attach, indexed:

{{EVIDENCE_LIST}}

I request that you:

1. Register this as a formal dispute and provide the **complaint reference number** in your reply;
2. Confirm the dispute category under which it has been registered;
3. Confirm the applicable timeline for resolution as per HDFC's grievance redressal policy, and — where the category provides for it — the initiation of the applicable card-network dispute process.

Please treat this email and its attachments as the complete first complaint. I will escalate per HDFC's published grievance redressal process if it is not resolved within the stated timeline.

Sincerely,
{{FULL_NAME}}
Card ending {{CARD_LAST4}}

---

> *This draft was prepared with an organisational tool, not by a lawyer. It is not legal advice. Verify all regulatory citations against the linked primary sources and all contact details against the bank's official page before sending. No outcome is predicted or guaranteed.*
