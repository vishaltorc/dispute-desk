---
title: HDFC Bank — escalation ladder (credit cards)
bank: hdfc
levels:
  - "Rung 1 — L1: credit card customer service"
  - "Rung 2 — L2: Grievance Redressal Officer, credit cards (Grievance Redressal Cell)"
  - "Rung 3 — L3/PNO: Principal Nodal Officer"
  - "Rung 4 — external: RBI Integrated Ombudsman (OUT OF SCOPE v1; reference only)"
source_url: https://www.hdfc.bank.in/need-help/grievance-redressal
last_verified: 2026-06-10
---

# HDFC escalation ladder — credit cards

HDFC publishes a **three-level internal** process for credit card grievances, then points externally to the RBI Ombudsman. Verified against HDFC's grievance pages on 2026-06-10 (see [contacts.md](contacts.md) for every address, phone, SLA, and source). The universal rules — one rung at a time, references everywhere, SLA discipline, consistent story — are in [procedure/escalation-ladder.md](../../procedure/escalation-ladder.md) and apply unchanged.

> **Template numbering note:** template files are numbered in the repo's generic order; on HDFC's actual ladder, [05-grievance-officer.md](templates/05-grievance-officer.md) serves **Rung 2** and [04-pno-escalation.md](templates/04-pno-escalation.md) serves **Rung 3**. Follow this ladder, not the filename numbers.

## Rung 1 — L1: Customer service (credit cards)

- **Contact:** [contacts.md → L1](contacts.md#l1--credit-card-customer-service) — phone banking (24×7), email, online form, post.
- **Trigger:** first complaint (decision-tree S0), a deflection response (S2), a chargeback demand (S4), or an amount correction (S6).
- **Templates:** [01-initial-dispute](templates/01-initial-dispute.md) · [02-reject-deflection](templates/02-reject-deflection.md) · [03-chargeback-demand](templates/03-chargeback-demand.md) · [07-amount-correction](templates/07-amount-correction.md).
- **Published SLA:** up to 10 working days.
- **Must come out of this rung:** the complaint reference number (gate G2). Without it, nothing above exists.
- **Do not accept as resolution:** "noted/forwarded" without a reference; advice to contact the merchant for a network-eligible category ([deflection D6](known-deflections.md)); closure without a written reason.

## Rung 2 — L2: Grievance Redressal Officer, credit cards

- **Contact:** [contacts.md → L2](contacts.md#l2--grievance-redressal-officer-credit-card-specific) — the **credit-card-specific** desk (parallel desks exist for banking/digital-lending; the wrong desk costs weeks).
- **Trigger:** gate G3 met against Rung 1 — its 10-working-day SLA lapsed, or its written outcome is wrong on facts / a [known deflection](known-deflections.md). Quote the L1 reference ("CRN") — HDFC's own page requires it.
- **Templates:** [05-grievance-officer](templates/05-grievance-officer.md) (primary); [03-chargeback-demand](templates/03-chargeback-demand.md) or [06-merchant-representment-rebuttal](templates/06-merchant-representment-rebuttal.md) where the situation is S4/S5 at this rung.
- **Published SLA:** up to 10 working days.
- **Do not accept as resolution:** a re-send of the L1 reply ([deflection D5](known-deflections.md)); a new reference that fragments the record — demand consolidation under the original CRN.

## Rung 3 — L3/PNO: Principal Nodal Officer

- **Contact:** [contacts.md → PNO](contacts.md#l3--pno--principal-nodal-officer). Note the email-domain caveat in contacts.md — re-check the source page before sending.
- **Trigger:** gate G3 met against Rung 2, **and** gate G4 (full package: cover sheet, timeline table, indexed evidence pack).
- **Template:** [04-pno-escalation](templates/04-pno-escalation.md).
- **Published SLA:** up to 10 working days.
- **Do not accept as resolution:** verbal assurances; "we are looking into it" past the SLA; resolution of a different question than the complaint asked.
- **Worth knowing:** HDFC's grievance policy routes complaints it intends to reject through an **Internal Ombudsman** whose decision binds the bank — a final written rejection should reflect that review (see the note in [contacts.md](contacts.md)).

## Rung 4 — External: RBI Integrated Ombudsman (reference only — OUT OF SCOPE v1)

- **HDFC's own published trigger:** unresolved after Levels 1–3, **or** no response within 30 days of lodging the complaint.
- **This repo stops here** (gate G5). The scheme, its preconditions, and why v1 doesn't walk the filing: [ombudsman-scheme-2021.md](../../regulations/rbi/ombudsman-scheme-2021.md). Keep the complete case file — references, replies, timeline, evidence pack — intact; any external forum starts by asking for exactly that.

## Timing math (worked from HDFC's published numbers)

Each internal rung publishes "up to 10 working days". The external trigger arms at **30 days from first lodging** regardless of rung — so a complaint that has properly climbed Rung 1 → 2 → 3 with G3 discipline will typically cross the 30-day mark during or after the PNO stage. Track both clocks (and the network chargeback window — gate G3 exception) from day one in the timeline table.
