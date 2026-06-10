---
title: HDFC Bank — verified grievance contacts (credit cards)
bank: hdfc
levels_published: 3 internal (L1 customer service → L2 grievance redressal officer → L3 PNO) + external RBI Ombudsman listed by HDFC as the next step
domain_note: >
  HDFC has migrated its website to hdfc.bank.in (the RBI-mandated .bank.in domain); old
  www.hdfcbank.com grievance URLs 301-redirect there. Most grievance emails have moved to
  @hdfc.bank.in, but the PNO address was still published on the old @hdfcbank.com domain at
  last verification — use addresses EXACTLY as listed below and re-check the source page.
policy_doc_url: https://www.hdfc.bank.in/content/dam/hdfcbankpws/in/en/personal-banking/discover-products/our-corporate-commitment/grievance-redressal-policy.pdf
policy_doc_version: "Customer Grievance Redressal Policy, Version 1.14, updated 2025-11-28"
last_verified: 2026-06-10
---

# HDFC Bank grievance contacts — credit cards

All values captured character-for-character from HDFC's official pages on **2026-06-10**. Contacts are perishable: re-check the `source_url` before sending, and surface the `last_verified` date to the user (HOW_AI_SHOULD_USE_THIS rule 4). Fields the bank does not publish are marked `NOT_PUBLISHED`, per [contact.schema.md](../../schema/contact.schema.md).

---

## L1 — Credit card customer service

```yaml
level: L1
name_or_desk: Customer Care — credit cards (phone banking, email, online form, branch, letter)
email: customerservices.cards@hdfc.bank.in
phone: "18001600 / 18002600 (accessible across India); from abroad +912261606160; services available 24x7 including Sundays and bank holidays"
postal_address: |
  Regular post: HDFC Bank Cards Division, P.O. Box 8654, Ambattur Industrial Estate P.O., Chennai - 600058
  Courier: HDFC Bank Cards Division, PO Box No 8654, Door No 94 SP, Estate Bus Stand, Wavin Main Road, Mogappair West, Chennai 600058
escalation_trigger: First contact — to register a complaint, query or request
sla_days: 10
source_url: https://www.hdfc.bank.in/need-help/grievance-redressal
last_verified: 2026-06-10
notes: |
  SLA as published: "up to 10 working days". Online complaint form:
  https://connect.hdfc.bank.in/applications/webforms/apply/HDFC_CustomerCenter/Customer_Center.aspx
  Emails/addresses from https://www.hdfc.bank.in/contact-us/write-to-us; phones from
  https://www.hdfc.bank.in/contact-us/customer-care. CAPTURE THE COMPLAINT REFERENCE NUMBER —
  gate G2 depends on it.
```

### L1 special desk — credit card mis-selling / harassment

```yaml
level: L1
name_or_desk: Dedicated desk for credit card mis-selling / harassment complaints
email: cardsales.complaint@hdfc.bank.in
phone: "044-61084900 (as displayed on the page)"
postal_address: NOT_PUBLISHED
escalation_trigger: Complaints specifically about mis-selling or harassment in credit card sales/recovery
sla_days: 10
source_url: https://www.hdfc.bank.in/need-help/grievance-redressal
last_verified: 2026-06-10
notes: Page anomaly — display text says "call at 044 - 61084900" but the underlying tel: link is 18002583838; the displayed number is recorded as primary. Re-check before relying on the phone channel.
```

## L2 — Grievance Redressal Officer (credit-card-specific)

```yaml
level: L2
name_or_desk: Mr. Shanmugasundar R — Grievance Redressal Officer for credit card specific complaints (Grievance Redressal Cell)
email: grievance.redressalcc@hdfc.bank.in
phone: "044-61084900 — Monday to Saturday 9:30am–5:30pm; not available on 2nd & 4th Saturdays, Sundays and bank holidays"
postal_address: |
  Grievance Redressal Cell, HDFC Bank Limited, HDFC Bank Cards Division,
  Door No. 94 SP, Estate Bus Stand, Wavin Main Road, Mogappair West, Chennai - 600058
escalation_trigger: "If Step 1 doesn't meet your expectations, contact our Grievance Redressal Officer with your previous complaint number" — keep the CRN/complaint reference ready
sla_days: 10
source_url: https://www.hdfc.bank.in/need-help/credit-card-specific-complaints
last_verified: 2026-06-10
notes: This is the credit-card track. Parallel L2 desks exist for banking/depository (Mr. Mehernosh Dhamodiwala) and digital lending (Ms. Shalini Tandon) — wrong desk = lost time; use the credit-card one for card disputes.
```

## L3 / PNO — Principal Nodal Officer

```yaml
level: PNO
name_or_desk: Mr. Ripal Kirtikumar Sheth — Principal Nodal Officer, HDFC Bank Ltd.
email: pnohdfcbank@hdfcbank.com
phone: "022-62841505 — Monday to Saturday 9:30am–5:30pm (excluding regional bank holidays, 2nd & 4th Saturdays)"
postal_address: |
  HDFC Bank Ltd., 5th Floor, Tower B, Peninsula Business Park,
  Lower Parel West, Mumbai 400013
escalation_trigger: "If the resolution at Step 2 does not meet your expectation, contact our Principal Nodal Officer"
sla_days: 10
source_url: https://www.hdfc.bank.in/need-help/grievance-redressal
last_verified: 2026-06-10
notes: |
  Email still on the OLD @hdfcbank.com domain at last verification while most others moved to
  @hdfc.bank.in — captured exactly as the official page's mailto link publishes it; RE-CHECK
  before sending. Regional/state nodal officers: nodal.officer@hdfc.bank.in (region-wise list at
  https://www.hdfc.bank.in/contact-us/email-id-for-nodal-officers; state-wise names/phones at
  https://www.hdfc.bank.in/contact-us/call-us).
```

## External — RBI Integrated Ombudsman (reference only; out of scope v1)

```yaml
level: L4
name_or_desk: Reserve Bank Integrated Ombudsman — EXTERNAL to HDFC; listed on HDFC's page as the step after L1–L3
email: NOT_PUBLISHED
phone: "14448 (RBI contact centre)"
postal_address: |
  Centralized Receipt and Processing Centre (CRPC), Reserve Bank of India,
  Central Vista, Sector 17, Chandigarh - 160017
escalation_trigger: "If your issue remains unresolved after contacting Level 1, Level 2 and Level 3, OR if you have not received response within 30 days of lodging a complaint" (as HDFC's page states)
sla_days: NOT_PUBLISHED
source_url: https://www.hdfc.bank.in/need-help/grievance-redressal
last_verified: 2026-06-10
notes: |
  Filing portal: https://cms.rbi.org.in. THIS REPO DOES NOT COVER THE FILING (v1 scope) — see
  procedure/preconditions.md gate G5 and regulations/rbi/ombudsman-scheme-2021.md. Recorded here
  because HDFC's own ladder names it and the 30-day trigger matters for timing the internal rungs.
```

---

## Bank-internal note: the Internal Ombudsman

HDFC's grievance policy (v1.14, link in front-matter) states that complaints the bank decides to **partially or wholly reject** are escalated to an **Internal Ombudsman** before the final reply, whose decision is binding on the bank. This is not a rung a customer writes to — but it means a written rejection should reflect Internal Ombudsman review, which is worth knowing when reading a final rejection letter.

## Overall SLA picture

Each published internal level states "up to 10 working days". The policy document sets per-grievance-type timelines with auto-escalation on breach rather than one global number. The **30-day no-response mark** is the trigger HDFC's own page publishes for the external (Ombudsman) step — consistent with the Credit Card Master Direction's ¶26(c) ([entry](../../regulations/rbi/credit-card-master-direction.md)).
