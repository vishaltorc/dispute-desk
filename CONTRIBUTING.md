---
title: Contributing to dispute-desk
type: governance
last_verified: 2026-06-10
---

# Contributing

Thank you. This repo only works if its contacts stay fresh, its citations stay verifiable, and its structure stays machine-readable. Contributions are reviewed against the rules below — they are the product.

## Adding a new bank (the main contribution path)

1. **Copy the skeleton.** Duplicate `banks/hdfc/` to `banks/<your-bank>/` (lowercase, hyphenated — `sbi-card`, `icici`, `axis`). The HDFC folder is the reference implementation of [schema/bank.schema.md](schema/bank.schema.md).
2. **Keep every file the schema requires:** `README.md`, `contacts.md`, `escalation-ladder.md`, `known-deflections.md`, and a `templates/` folder. Delete nothing; replace content.
3. **Re-source everything.** Nothing in the HDFC folder carries over factually. Every contact, SLA, and escalation level must come from *your* bank's official pages, fetched at contribution time.
4. **Conform to the schemas.** Front-matter fields are defined in [schema/](schema/): [contact.schema.md](schema/contact.schema.md), [template.schema.md](schema/template.schema.md), [regulation.schema.md](schema/regulation.schema.md). A file that doesn't conform will be rejected — AI assistants navigate by these fields.
5. **Bank-agnostic content goes in `procedure/`, not your bank folder.** If you find yourself writing escalation logic that applies to every bank, it belongs in the shared layer.

## Verification rules (non-negotiable)

- **`last_verified` + `source_url` on every contact and every regulation entry.** The date is the day *you* loaded the official page and saw the value — not the day you remembered it.
- **Official domains only.** Bank contacts from the bank's own domain; RBI material from rbi.org.in; network rules from the network's own domain; NPCI from npci.org.in. Blog posts, aggregators, and forum threads are never verification sources (they may help you *find* the official page).
- **Cannot verify → mark `UNVERIFIED`.** An honest `UNVERIFIED` with a note is welcome; a guessed value is grounds for rejection.
- **No reproduction of regulatory full-text.** Link the official document; quote clause references and one-line descriptions only.
- **Plain-English summaries are labelled.** Every regulation summary carries the line "Plain-English summary — verify against the source before relying on this."
- **Re-verification cadence:** contacts should be re-checked roughly every 6 months. If you load a source page and the value still matches, bump `last_verified` to today — that bump alone is a valuable PR.

## Content rules

- **No outcome predictions.** Nothing in this repo may state or imply that a user will win, lose, or how likely either is.
- **No real personal data — yours or anyone's.** Templates use `{{UPPER_SNAKE}}` placeholders. Examples are fully synthetic. Do not commit your own statements, screenshots, or reference numbers, and never accept a contribution containing someone's real data.
- **No fabricated reference numbers or amounts**, even as examples — use obviously-synthetic values and label them.
- **Tone: factual, not inflammatory.** Deflection catalogues document patterns and counters; they do not name-and-shame individuals or editorialise. A repo that reads like a grudge loses the credibility that makes its drafts effective.
- **Markdown only, UTF-8, lowercase hyphenated paths.** No build steps, no proprietary formats — the raw repo is the product.

## PR checklist

- [ ] Every new/changed contact has `last_verified` (today) and an official `source_url`
- [ ] Every new/changed regulation entry has `official_reference`, `source_url`, `last_verified`, and a labelled plain-English summary
- [ ] Every template's `{{TOKENS}}` are all listed in its front-matter `placeholders`
- [ ] No real PII, no fabricated-but-plausible reference numbers, no outcome predictions
- [ ] Submission-bound templates end with the short-form disclaimer block from [DISCLAIMER.md](DISCLAIMER.md)
- [ ] New bank folders conform to [schema/bank.schema.md](schema/bank.schema.md)
- [ ] INDEX.md updated if you added or moved files
