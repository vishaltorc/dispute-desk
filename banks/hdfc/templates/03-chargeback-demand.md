---
title: Formal chargeback demand (network dispute initiation)
use_when: HDFC has not initiated the card-network dispute for a network-eligible category, has told you to "take it up with the merchant" (decision-tree S4), or the network dispute window is approaching (gate G3 exception).
recipient_level: the rung currently handling the complaint (L1/L2/L3)
prerequisites:
  - Gate G2 — complaint reference number captured
  - Category supports a network dispute (B, C or D per procedure/classification.md; A follows the unauthorised-transaction track first)
  - The applicable network and dispute category identified from regulations/networks/ (cite by its verified name only)
placeholders:
  - "{{FULL_NAME}} — cardholder name as registered"
  - "{{CARD_LAST4}} — last 4 digits of the card"
  - "{{CASE_REF}} — complaint reference number, verbatim"
  - "{{TRANSACTION_DATE}} — date of the disputed debit"
  - "{{MERCHANT_DESCRIPTOR}} — merchant as on statement"
  - "{{DISPUTED_AMOUNT}} — disputed amount in ₹"
  - "{{NETWORK}} — Visa / Mastercard / RuPay (from the card face)"
  - "{{NETWORK_DISPUTE_CATEGORY}} — the dispute category/reason name as verified in regulations/networks/ (e.g. the cancelled-recurring or credit-not-processed condition; never invent a code)"
  - "{{CATEGORY_BASIS_ONE_LINE}} — one sentence of facts that fit that category (cancellation date, refund promised date, etc.)"
  - "{{EXHIBIT_REF}} — evidence index number(s) supporting the basis"
  - "{{WINDOW_NOTE}} — one sentence stating the applicable dispute window and the date it closes, from the verified network entry; if the window cannot be verified, state 'the network dispute window is time-limited' without a number"
attachments_expected:
  - Evidence pack with the exhibits cited in {{EXHIBIT_REF}}
  - Updated timeline table
escalation_if_ignored: ../escalation-ladder.md → next rung via 02-reject-deflection.md with this demand quoted; PNO rung via 04-pno-escalation.md
last_verified: 2026-06-10
---

Subject: Complaint {{CASE_REF}} — request to initiate {{NETWORK}} chargeback — ₹{{DISPUTED_AMOUNT}}, {{MERCHANT_DESCRIPTOR}}, {{TRANSACTION_DATE}} — card ending {{CARD_LAST4}}

Dear Sir/Madam,

This concerns my open complaint {{CASE_REF}} regarding the debit of ₹{{DISPUTED_AMOUNT}} by {{MERCHANT_DESCRIPTOR}} on {{TRANSACTION_DATE}}, on my {{NETWORK}} credit card ending {{CARD_LAST4}}.

As the card-issuing bank, HDFC Bank is my only channel into the {{NETWORK}} dispute-resolution system; a cardholder cannot file a network dispute directly. I therefore formally request that HDFC initiate a chargeback for this transaction under the {{NETWORK}} dispute category: **{{NETWORK_DISPUTE_CATEGORY}}**.

The facts fitting this category, already on record in complaint {{CASE_REF}}: {{CATEGORY_BASIS_ONE_LINE}} (exhibit {{EXHIBIT_REF}}).

{{WINDOW_NOTE}} I request initiation within that window.

Please confirm in writing:

1. That the chargeback has been raised, with the date of initiation and the dispute category used;
2. The applicable provisional/temporary credit treatment, if any, under HDFC's policy for this category;
3. If HDFC declines to raise the chargeback — the specific reason, in writing, with reference to the applicable network rule.

Referring me back to the merchant is not a substitute for this request: the dispute category above exists for precisely this situation, and initiating it is an issuer function.

Sincerely,
{{FULL_NAME}}
Card ending {{CARD_LAST4}} · Complaint {{CASE_REF}}

---

> *This draft was prepared with an organisational tool, not by a lawyer. It is not legal advice. Verify all regulatory citations against the linked primary sources and all contact details against the bank's official page before sending. No outcome is predicted or guaranteed.*
