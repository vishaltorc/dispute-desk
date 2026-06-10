---
title: RuPay dispute rules (NPCI)
regulator: RuPay (NPCI)
official_reference: "RuPay Dispute Management Rules and Regulations manual, Version 6.0 — member-bank access only (BCS RuPay Portal); public reason-code table: UNVERIFIED"
source_url: https://www.npcisupport.org.in/portal/en/kb/articles/dispute-tat
last_verified: 2026-06-10
applies_to: disputes on RuPay-branded cards; processed by the issuing bank through NPCI's dispute-management system
plain_english_summary: >
  NPCI does not publish RuPay chargeback reason codes publicly. The governing document — the
  RuPay Dispute Management Rules and Regulations manual (v6.0) — lives behind NPCI's member-bank
  portal. Practical consequence for a cardholder: you cannot cite a RuPay reason code the way you
  can a Visa or Mastercard one; the dispute is filed by your issuing bank, which has access to the
  manual, and your demand should name the fact pattern and ask the bank to file under the
  applicable RuPay dispute category.
key_clauses:
  - "Governing document — 'RuPay Dispute Management Rules and Regulations manual Version 6.0', confirmed by NPCI's support knowledge base as available in the BCS RuPay Portal (member banks only)"
  - "Public reason-code table — UNVERIFIED: no official public page lists RuPay reason codes as of last_verified"
  - "Dispute turnaround details — UNVERIFIED for the same reason; they sit inside the member-access manual"
status: UNVERIFIED
---

# RuPay dispute rules

**Plain-English summary — verify against the source before relying on this.**

**Status: UNVERIFIED — and that is the verified finding.** Unlike Visa and Mastercard, whose public rulebooks let this repo cite named dispute conditions, NPCI's RuPay dispute rules are bank-facing: the governing manual (v6.0) is confirmed to exist by [NPCI's own support portal](https://www.npcisupport.org.in/portal/en/kb/articles/dispute-tat) but is accessible only to member banks. An earlier public copy of the manual (v5) and several legacy NPCI circular URLs now return NPCI's page-not-found shell after a site migration; NPCI's former public chargeback page now redirects to ecosystem statistics. Related official pages: [RuPay circulars index](https://www.npci.org.in/what-we-do/rupay/circulars).

## What this means for a RuPay dispute (practical, not regulatory)

1. **Don't cite a reason code you can't verify.** The [chargeback demand template](../../banks/hdfc/templates/03-chargeback-demand.md) instructs the AI never to invent a code; for RuPay, `{{NETWORK_DISPUTE_CATEGORY}}` becomes a *named fact pattern* — e.g. "the RuPay dispute category applicable to a recurring debit processed after mandate withdrawal" — with an explicit request that the bank, which has manual access, identify and file under it.
2. **The RBI layer still fully applies.** The e-mandate framework, the limited-liability rules, and the Master Direction's billing-dispute clauses ([rbi/](../rbi/)) are issuer obligations independent of the card network. A RuPay category-B dispute leans harder on those — which is no small lean.
3. **The bank cannot claim there is no dispute mechanism.** NPCI operates a dispute-management system through which member banks process RuPay chargebacks (and publishes monthly chargeback volumes); a written "RuPay has no chargeback process" reply would contradict NPCI's own published statistics page and should be countered as a [D6-pattern deflection](../../banks/hdfc/known-deflections.md) requesting the bank's written basis.

## Re-verification note

If NPCI republishes the manual or a public reason-code table, this entry should be upgraded: replace `UNVERIFIED` with the verified references, keep this page's history. Check the [circulars index](https://www.npci.org.in/what-we-do/rupay/circulars) first.

## Related

- [Visa](visa-reason-codes.md) · [Mastercard](mastercard-reason-codes.md)
- [classification.md](../../procedure/classification.md) — fact patterns still classify identically; only the code citation differs
