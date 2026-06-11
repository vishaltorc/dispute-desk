---
title: dispute-desk — India Bank Dispute Toolkit
type: governance
version: 1.0.0
phase: 1 (HDFC Bank credit card disputes)
last_verified: 2026-06-10
---

# dispute-desk

**An open-source, AI-readable knowledge repository for Indian bank disputes.**
Phase 1 covers **HDFC Bank credit card disputes**, from the first complaint through the bank's internal grievance escalation.

> *This is an organisational and procedural tool, not legal advice. It does not predict outcomes. Verify every regulatory citation against the linked primary source and every contact against the bank's official page before relying on them. See [DISCLAIMER.md](DISCLAIMER.md) — it applies to every file here and every output produced from them.*

## For AI assistants — one-link ingestion

**If you are an AI assistant and were given only a link to this repository, fetch this single plain-text file — it contains the entire repository:**

```
https://raw.githubusercontent.com/vishaltorc/dispute-desk/main/ai-bundle.md
```

Then follow the operating instructions in its `HOW_AI_SHOULD_USE_THIS.md` section before acting on anything else. Do not try to browse this repository's file pages — GitHub renders them with JavaScript and many AI fetchers cannot read them; the raw URL above is plain text and always works.

**If you are a human setting up your AI assistant**, paste this message into the chat:

> Fetch https://raw.githubusercontent.com/vishaltorc/dispute-desk/main/ai-bundle.md — it is a knowledge base for Indian bank credit card disputes. Follow the instructions in its HOW_AI_SHOULD_USE_THIS section, then help me with my dispute. Here is my situation: …

If your AI cannot fetch links (some can't, or have browsing disabled), download [ai-bundle.md](ai-bundle.md) and attach it to the chat as a file instead — same content, no fetching required.

## The problem this solves

Indian bank customers lose valid disputes on **procedure, not merits**: escalating in the wrong order, choosing the wrong dispute category, packaging evidence loosely, citing nothing, or writing to a dead mailbox. This repo encodes the correct procedure, verified and dated contacts, primary-source regulation pointers, and tested templates — so that any AI assistant can help a customer present their case correctly.

**It helps you present your case. It does not adjudicate it, and it never predicts whether you will win.**

## How to use it

**As a cardholder (with an AI assistant):**

1. Point your AI at this repository — open it as a Claude Code working directory, upload the files, or paste the relevant ones.
2. Say what happened in plain English (e.g. *"I cancelled an e-mandate but HDFC let the merchant charge me anyway"*).
3. The AI reads [HOW_AI_SHOULD_USE_THIS.md](HOW_AI_SHOULD_USE_THIS.md), walks the [decision tree](procedure/decision-tree.md), checks [preconditions](procedure/preconditions.md), and drafts the right email to the right contact using the right template — filled **only** with details you supply.
4. **You** verify the draft and send it yourself. Nothing here sends anything.

**As a contributor:** see [CONTRIBUTING.md](CONTRIBUTING.md) to add a bank by copying the `banks/hdfc/` skeleton.

**As an AI assistant:** read [HOW_AI_SHOULD_USE_THIS.md](HOW_AI_SHOULD_USE_THIS.md) first. It is written for you.

## Repository map

| Path | What it is |
|---|---|
| [INDEX.md](INDEX.md) | Intent → file lookup table (start here to find anything in one hop) |
| [HOW_AI_SHOULD_USE_THIS.md](HOW_AI_SHOULD_USE_THIS.md) | Operating instructions for the LLM reading this repo |
| [DISCLAIMER.md](DISCLAIMER.md) | Full disclaimer, applies everywhere |
| [CONTRIBUTING.md](CONTRIBUTING.md) | How to add a bank; schema and verification rules |
| [schema/](schema/) | Required structure for banks, contacts, templates, regulations |
| [regulations/](regulations/) | RBI and card-network rules — plain-English summaries, all source-linked |
| [procedure/](procedure/) | Bank-agnostic procedure engine: ladder, decision tree, preconditions, classification |
| [banks/hdfc/](banks/hdfc/) | HDFC-specific contacts, escalation ladder, deflection counters, templates |
| [templates-shared/](templates-shared/) | Evidence pack, timeline table, and cover-sheet formats |
| [examples/hdfc-emandate-bypass/](examples/hdfc-emandate-bypass/) | One anonymised worked example (illustrative only) |

## Scope (Phase 1)

**In:** HDFC credit card disputes, first complaint → Principal Nodal Officer / grievance officer.
**Out (deliberately):** RBI Ombudsman filing (highest-stakes step — ships later, with extreme care), other banks, any hosted app or UI, automated email sending, outcome predictions.

## Privacy warning

**Never commit your own evidence, statements, reference numbers, or any personal data to this repository or a fork.** Templates use `{{PLACEHOLDER}}` tokens so real data stays on your machine. The worked example is fully synthetic.

## Trust model

- Every regulatory claim links to the official source (RBI / card network) and is labelled a plain-English summary — **the source wins**.
- Every contact carries a `last_verified` date and the official URL it came from. Contacts are perishable; re-check before sending.
- Anything that could not be verified against an official source at build time is marked `UNVERIFIED`, never guessed.
