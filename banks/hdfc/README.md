---
title: HDFC Bank — bank-specific dispute pack
bank: hdfc
products_covered: credit cards (Phase 1)
last_verified: 2026-06-10
---

# HDFC Bank

The bank-specific layer for HDFC credit card disputes. Universal procedure (classification, gates, the abstract ladder) lives in [`procedure/`](../../procedure/); this folder holds only what is HDFC's own: contacts, the concrete escalation ladder, observed deflection patterns, and addressed templates.

## Folder map

| File | What it is |
|---|---|
| [contacts.md](contacts.md) | Every escalation contact, with `last_verified` dates and official source URLs |
| [escalation-ladder.md](escalation-ladder.md) | HDFC's rung-by-rung ladder, mapping each rung to a contact and a template |
| [known-deflections.md](known-deflections.md) | Documented stall patterns + factual counters |
| [templates/](templates/) | Seven templates, numbered in rough escalation order |

## HDFC quirks worth knowing

- **Two email domains.** HDFC has used both `@hdfcbank.com` and `@hdfc.bank.in` addresses for grievance contacts. Always use the address exactly as it appears in [contacts.md](contacts.md), and re-check its `source_url` before sending — domain-level typos silently kill escalations.
- **Credit cards have their own grievance track.** HDFC publishes credit-card-specific grievance contacts alongside general banking ones; the credit-card track is the one this folder documents.
- **Reference number discipline matters here.** HDFC's levels check whether the level below was exhausted by reference number. The non-negotiable output of every interaction is a reference captured verbatim (gate G2).

## Freshness

Contacts are perishable. Every entry in [contacts.md](contacts.md) carries the date it was last verified against HDFC's official page and the URL it came from. If a `last_verified` date is more than ~6 months old, re-check the source before sending — and bump the date in a PR if values still match (see [CONTRIBUTING.md](../../CONTRIBUTING.md)).

> *Reminder: this folder is an organisational and procedural tool, not legal advice, and it predicts no outcomes. [Full disclaimer](../../DISCLAIMER.md).*
