# dispute-desk — single-file AI bundle (generated)

> This file concatenates the entire dispute-desk repository (Phase 1: HDFC Bank credit
> card disputes) into one document for upload/paste into any AI assistant. Canonical
> source: https://github.com/vishaltorc/dispute-desk — regenerate this bundle when the
> repo changes; in any conflict, the individual repo files win.
>
> AI assistants: the operating instructions are in the HOW_AI_SHOULD_USE_THIS.md section
> below. Read it before acting on anything else. This is an organisational and procedural
> tool, not legal advice, and it predicts no outcomes (see DISCLAIMER.md section).
>
> Each original file begins at a line of the form:  ===== FILE: <path> =====



===== FILE: README.md =====

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


===== FILE: DISCLAIMER.md =====

---
title: Full disclaimer
type: governance
applies_to: every file in this repository and every output produced from it
last_verified: 2026-06-10
---

# Disclaimer

This disclaimer applies to **every file in this repository** and to **every draft, summary, or recommendation an AI assistant produces using this repository**.

## 1. Not legal advice

dispute-desk is an **organisational and procedural tool**. It helps you structure a complaint, follow a bank's published grievance process in the correct order, and present your own facts clearly.

It is **not legal advice**, and using it does not create any advisor–client relationship. If your dispute involves significant money, fraud, or legal threats, consult a qualified professional.

## 2. Verify everything against primary sources

Every regulatory statement in this repository is a **plain-English summary written for navigation only**. Summaries can be wrong, incomplete, or out of date. Each regulation entry links to the official source document — **read the source before relying on any claim**. If a summary and the source disagree, the source wins.

## 3. No outcome predictions

This repository does not predict whether any dispute will succeed, and no AI assistant using it should do so. Banks, card networks, and the RBI decide disputes on their own facts. A procedurally correct complaint can still be rejected on merits. **If an AI using this repo tells you that you "will win" or that an outcome is "guaranteed", it is misusing this repo — disregard that claim.**

## 4. Contacts are perishable

Bank contact details (emails, phone numbers, nodal officers, addresses) change without notice. Every contact entry here carries a `last_verified` date and the official source URL it came from. **Re-check the source URL before sending anything**, especially if the `last_verified` date is more than a few months old.

## 5. Your data is yours — keep it out of the repo

Never commit your own statements, screenshots, reference numbers, card numbers, or any personal data to this repository or any fork of it. Templates use `{{PLACEHOLDER}}` tokens precisely so that real data stays on your machine.

## 6. You send the email, not the AI

This repository produces **drafts**. A human must review every draft, verify every fact in it, and send it themselves. Nothing here automates sending.

---

### Short-form disclaimer block

The block below is reproduced at the foot of every submission-bound template. It is the canonical short form of this document:

> *This draft was prepared with an organisational tool, not by a lawyer. It is not legal advice. Verify all regulatory citations against the linked primary sources and all contact details against the bank's official page before sending. No outcome is predicted or guaranteed.*


===== FILE: HOW_AI_SHOULD_USE_THIS.md =====

---
title: How an AI assistant must use this repository
type: governance
audience: the LLM reading this repo (Claude, ChatGPT, Gemini, or any other)
last_verified: 2026-06-10
---

# HOW AI SHOULD USE THIS

You are an AI assistant helping a human with an Indian bank dispute. This repository is your source of truth for **procedure, contacts, templates, and regulation pointers**. The human is your source of truth for **facts**. Follow these rules exactly.

## Operating sequence

1. **Locate the user's state first.** Read [procedure/decision-tree.md](procedure/decision-tree.md) and match the user's plain-English situation to a state. If you cannot match a state, ask the user clarifying questions — do not guess.
2. **Classify before you draft.** Use [procedure/classification.md](procedure/classification.md) to determine the dispute category (unauthorised vs authorised-but-disputed, etc.). The category changes which rules apply and which template is correct. State your classification to the user and why.
3. **Gate every step on its preconditions.** Before recommending any escalation step, check [procedure/preconditions.md](procedure/preconditions.md). If a precondition is unmet, say so, say **why** the step is blocked, and help the user complete the missing precondition instead. Never skip ahead because the user is frustrated.
4. **Pull contacts only from the bank's contacts file** ([banks/hdfc/contacts.md](banks/hdfc/contacts.md)). When you give the user a contact, **always surface its `last_verified` date and `source_url`** and tell the user to re-check the source page before sending. Never supply a bank contact from your own training data.
5. **Use the matching template.** Each decision-tree outcome names a template in [banks/hdfc/templates/](banks/hdfc/templates/). Use it. Fill `{{PLACEHOLDER}}` tokens **only from values the user has explicitly given you**. If a value is missing, ask. **Never invent reference numbers, dates, amounts, or names. Never leave a placeholder silently unfilled.**
6. **Cite by linking, never by asserting.** When you mention a regulation, link the entry in [regulations/](regulations/) which links the official source. Never assert what a regulation says without that link. If the repo marks something `UNVERIFIED`, tell the user it is unverified.
7. **Restate the disclaimer with every submission-bound draft.** Every draft email or letter you produce must end with the short-form disclaimer block from [DISCLAIMER.md](DISCLAIMER.md). Do not strip it.

## Hard prohibitions

- **Never predict the outcome.** Do not say or imply the user "will win", has a "strong case", is "guaranteed" a refund, or any probability of success. You help the user present their case correctly; you do not adjudicate it. If asked "will I win?", explain that this tool organises procedure and evidence and does not predict outcomes.
- **Never fabricate.** No invented reference numbers, circular numbers, clause numbers, amounts, contact details, or deadlines. Missing fact → ask the user. Missing regulation detail → point at the source link and say you have not verified beyond it.
- **Never send anything.** You produce drafts. The human reviews, verifies, and sends.
- **Never advise on the RBI Ombudsman filing itself.** It is out of scope for this version of the repo (see README scope). You may explain that the bank-level process must be exhausted first, and you may point at [regulations/rbi/ombudsman-scheme-2021.md](regulations/rbi/ombudsman-scheme-2021.md) as reference, but do not walk the user through filing.
- **Never let the user's anger set the tone.** Drafts stay factual and civil — see the tone rules in each template. Factual escalation outperforms inflammatory escalation, and this repo carries no naming-and-shaming language.
- **Never ask the user to put real personal data into this repo or a fork.** Evidence stays on their machine.

## Interview pattern for filling a template

When a template's front-matter lists placeholders, run a short interview — one compact message, not twenty questions:

> "To fill the dispute email I need: (1) the last 4 digits of your card, (2) the disputed amount and date as they appear on the statement, (3) the merchant name as it appears, (4) your complaint reference number if you already have one, (5) what HDFC last told you, in one line."

Then fill the template verbatim from the answers. Quote amounts and dates exactly as the user gave them; do not normalise currency or reformat dates inside the draft body without telling the user.

## When the repo and reality disagree

If the user reports that a contact bounced, a page moved, or a rule changed: trust the user's observation, tell them the repo entry may be stale (check its `last_verified` date), and direct them to the `source_url` to find the current detail. Suggest they (or you, if you have the capability) open an issue or PR updating the entry with a new `last_verified` date.

## One-hop lookup

[INDEX.md](INDEX.md) maps user intents to file paths. Use it when you need to find something fast.


===== FILE: INDEX.md =====

---
title: INDEX — intent → file lookup
type: index
note: generated at build time; update when files are added or moved (CONTRIBUTING.md checklist)
last_verified: 2026-06-10
---

# INDEX

One-hop lookup from what you (or the user) need to the file that has it. AI assistants: read [HOW_AI_SHOULD_USE_THIS.md](HOW_AI_SHOULD_USE_THIS.md) before using anything below.

## Start here

| Intent | File |
|---|---|
| Understand what this repo is and its limits | [README.md](README.md) |
| The disclaimer that applies to everything | [DISCLAIMER.md](DISCLAIMER.md) |
| Operating instructions for an AI assistant | [HOW_AI_SHOULD_USE_THIS.md](HOW_AI_SHOULD_USE_THIS.md) |
| Add a bank / contribute | [CONTRIBUTING.md](CONTRIBUTING.md) |

## "Help me with my dispute" (procedure)

| Intent | File |
|---|---|
| Find the user's current state and the single correct next step | [procedure/decision-tree.md](procedure/decision-tree.md) |
| Check whether a step is allowed yet (gates G0–G5) | [procedure/preconditions.md](procedure/preconditions.md) |
| Pick the correct dispute category (this decides everything) | [procedure/classification.md](procedure/classification.md) |
| Understand the escalation order and why skipping rungs fails | [procedure/escalation-ladder.md](procedure/escalation-ladder.md) |

## HDFC specifics

| Intent | File |
|---|---|
| Who to write to, with freshness dates and sources | [banks/hdfc/contacts.md](banks/hdfc/contacts.md) |
| HDFC's actual rung order, SLAs, and which template per rung | [banks/hdfc/escalation-ladder.md](banks/hdfc/escalation-ladder.md) |
| The bank replied with a non-answer — match and counter it | [banks/hdfc/known-deflections.md](banks/hdfc/known-deflections.md) |
| HDFC quirks (domain migration, parallel desks) | [banks/hdfc/README.md](banks/hdfc/README.md) |

## Drafting (HDFC templates)

| Situation (decision-tree state) | Template |
|---|---|
| First complaint, any category (S0) | [01-initial-dispute](banks/hdfc/templates/01-initial-dispute.md) |
| Reply doesn't address the complaint (S2, S9) | [02-reject-deflection](banks/hdfc/templates/02-reject-deflection.md) |
| Bank won't raise the network dispute / window closing (S4) | [03-chargeback-demand](banks/hdfc/templates/03-chargeback-demand.md) |
| Escalate to the PNO — Rung 3 (S3) | [04-pno-escalation](banks/hdfc/templates/04-pno-escalation.md) |
| Escalate to the Grievance Redressal Officer — Rung 2 (S3) | [05-grievance-officer](banks/hdfc/templates/05-grievance-officer.md) |
| Merchant's representment accepted (S5) | [06-merchant-representment-rebuttal](banks/hdfc/templates/06-merchant-representment-rebuttal.md) |
| Credit posted but the amount is wrong (S6) | [07-amount-correction](banks/hdfc/templates/07-amount-correction.md) |

## Evidence formats (any bank)

| Intent | File |
|---|---|
| Assemble the numbered evidence pack | [templates-shared/evidence-index.md](templates-shared/evidence-index.md) |
| Build the chronological timeline table | [templates-shared/timeline-table.md](templates-shared/timeline-table.md) |
| Cover sheet for a PDF submission | [templates-shared/document-cover.md](templates-shared/document-cover.md) |

## Regulations (all source-linked; summaries are navigation only)

| Intent | File |
|---|---|
| Regulation index with "use when" guidance | [regulations/README.md](regulations/README.md) |
| Recurring charge after cancellation / missing pre-debit notice | [regulations/rbi/recurring-payments-emandate.md](regulations/rbi/recurring-payments-emandate.md) |
| Unauthorised transaction — liability bands, burden of proof | [regulations/rbi/unauthorised-transactions-liability.md](regulations/rbi/unauthorised-transactions-liability.md) |
| Billing protests, disputed-charge fees, bureau reporting, grievance machinery | [regulations/rbi/credit-card-master-direction.md](regulations/rbi/credit-card-master-direction.md) |
| What exists above the bank (reference only; filing out of scope) | [regulations/rbi/ombudsman-scheme-2021.md](regulations/rbi/ombudsman-scheme-2021.md) |
| Visa dispute condition to cite | [regulations/networks/visa-reason-codes.md](regulations/networks/visa-reason-codes.md) |
| Mastercard reason code to cite | [regulations/networks/mastercard-reason-codes.md](regulations/networks/mastercard-reason-codes.md) |
| RuPay — what is (and isn't) publicly citable | [regulations/networks/rupay-dispute-rules.md](regulations/networks/rupay-dispute-rules.md) |

## Worked example (synthetic, illustrative only)

| Intent | File |
|---|---|
| See the whole flow on one fact pattern | [examples/hdfc-emandate-bypass/narrative.md](examples/hdfc-emandate-bypass/narrative.md) |
| See the timeline-table format in use | [examples/hdfc-emandate-bypass/timeline.md](examples/hdfc-emandate-bypass/timeline.md) |
| The transferable mechanics, minus the one-off facts | [examples/hdfc-emandate-bypass/what-worked.md](examples/hdfc-emandate-bypass/what-worked.md) |

## Schemas (for contributors and validators)

| Intent | File |
|---|---|
| Required structure of a bank folder | [schema/bank.schema.md](schema/bank.schema.md) |
| Required fields of a contact entry | [schema/contact.schema.md](schema/contact.schema.md) |
| Required front-matter of a template | [schema/template.schema.md](schema/template.schema.md) |
| Required fields of a regulation entry | [schema/regulation.schema.md](schema/regulation.schema.md) |


===== FILE: procedure/decision-tree.md =====

---
title: Decision tree — from user state to the single correct next step
type: procedure
scope: an AI walks this with the user; every external step is precondition-gated
last_verified: 2026-06-10
---

# Decision tree

Match the user's situation to a state below. Each state yields **one correct next step**, the template to use, and the gates that must pass first ([preconditions.md](preconditions.md)). If two states seem to match, the more specific one wins. If none match, interview the user until one does — do not improvise a path.

Templates referenced are HDFC's (`banks/hdfc/templates/`); for another bank, the same-numbered template in its folder.

## How to read a state

```
STATE — how the user typically describes it
→ NEXT STEP (recipient level) | TEMPLATE | GATES
```

---

### S0 — "I just found a charge I want to dispute" (nothing filed yet)

First: classify ([classification.md](classification.md)).

- **S0a — category A (unauthorised):**
  → File the dispute **immediately** (L1) | [01-initial-dispute](../banks/hdfc/templates/01-initial-dispute.md) | gates G0, G1.
  Reporting delay changes the user's liability — same-day filing matters ([liability entry](../regulations/rbi/unauthorised-transactions-liability.md)). Also follow the bank's card-blocking guidance for actual fraud; for *suspected-but-unsure*, see S8 first.
- **S0b — category B (cancelled mandate / recurring charged anyway):**
  → File the dispute (L1) | [01-initial-dispute](../banks/hdfc/templates/01-initial-dispute.md) | gates G0, G1.
  The complaint cites the e-mandate framework ([entry](../regulations/rbi/recurring-payments-emandate.md)) and demands the charge be treated under it.
- **S0c — category C (service/billing, merchant reachable):**
  → One written merchant attempt with a deadline (rung 0) — then L1 with proof of that attempt | [01-initial-dispute](../banks/hdfc/templates/01-initial-dispute.md) | gates G0, G1.
- **S0d — category D (amount error / duplicate / promised refund not received):**
  → File at L1 | [01-initial-dispute](../banks/hdfc/templates/01-initial-dispute.md) (for missing refunds the ask is the credit; for a wrong refund amount already received, use [07-amount-correction](../banks/hdfc/templates/07-amount-correction.md)) | gates G0, G1.

### S1 — "I complained, they gave me a reference, nothing has happened yet" (SLA still running)

→ **Wait the SLA out; build the package.** No external send. | no template | —
Assemble [timeline table](../templates-shared/timeline-table.md) and [evidence index](../templates-shared/evidence-index.md) so the escalation is ready the day the SLA lapses. Diarise the lapse date. *Exception:* if the network chargeback window closes before the SLA (gate G3 exception) → S4 now.

### S2 — "The bank replied with something that doesn't address my complaint" (deflection)

Typical lines: "please cancel the mandate yourself", "no debit found", "block your card first", a re-sent older reply.
→ Reject the deflection in writing at the **same rung** | [02-reject-deflection](../banks/hdfc/templates/02-reject-deflection.md) | gates G0–G2; check the reply against [known-deflections](../banks/hdfc/known-deflections.md) and cite the matching counter.
A deflection rejected in writing converts into a G3 escalation trigger if repeated.

### S3 — "SLA expired / they closed it without fixing it" (escalation up one rung)

→ Escalate **one** rung (L2 if coming from L1; L3 if from L2) | [04-pno-escalation](../banks/hdfc/templates/04-pno-escalation.md) only when the next rung is PNO, otherwise [02-reject-deflection](../banks/hdfc/templates/02-reject-deflection.md) restructured per the bank ladder (`banks/hdfc/escalation-ladder.md` names the right template per rung) | gates G2, G3 (+ G4 from L3 up).

### S4 — "The bank won't raise a chargeback / says it's between me and the merchant"

→ Formal chargeback demand at the current rung | [03-chargeback-demand](../banks/hdfc/templates/03-chargeback-demand.md) | gates G0–G2.
The demand names the applicable network dispute category ([Visa](../regulations/networks/visa-reason-codes.md) / [Mastercard](../regulations/networks/mastercard-reason-codes.md) / [RuPay](../regulations/networks/rupay-dispute-rules.md)) and the window date. The issuing bank is the user's only door into the network dispute system — "deal with the merchant" is not a complete answer for network-eligible categories (see known-deflections).

### S5 — "Bank says the merchant responded/proved the charge and re-applied it" (representment)

→ Rebut the representment with evidence, at the rung where the chargeback was handled | [06-merchant-representment-rebuttal](../banks/hdfc/templates/06-merchant-representment-rebuttal.md) | gates G0–G3 + **demand a copy of the merchant's representment documents** if not provided — the rebuttal must answer what the merchant actually submitted, not a guess.

### S6 — "They refunded, but the amount is wrong / fees and interest from the disputed charge weren't reversed"

→ Amount-correction request at the rung that issued the credit | [07-amount-correction](../banks/hdfc/templates/07-amount-correction.md) | gates G0, G2.
The ask itemises: principal, late fees, interest, GST on fees, and (category A) the liability rule the itemisation rests on.

### S7 — "PNO level done — SLA lapsed or final rejection in hand"

→ **Boundary of this repo (v1).** | no template | gate G5.
Tell the user plainly: the internal ladder is exhausted; the RBI Ombudsman scheme exists with its own preconditions and time limits ([reference entry](../regulations/rbi/ombudsman-scheme-2021.md)); read the scheme document at the official source before acting. Do not walk the filing. Help them keep the complete case file intact — it is exactly what any next forum will need.

### S8 — "I'm not sure this charge is fraud — I might have authorised something"

→ **Classify before filing anything** ([classification.md](classification.md)) | no template | gate G1.
Filing "fraud" for an authorised-but-disputed charge can trigger card blocking and an investigation track that doesn't fit the facts; filing "billing dispute" for genuine fraud surrenders the liability-window protections. Interview, classify, then go to S0.

### S9 — "It's been charged again this cycle while the dispute is open" (recurring continues)

→ Two-part step at current rung: (a) add the new debit to the open complaint (same reference — do **not** open a fresh complaint), (b) if category B, demand mandate-level stoppage citing the e-mandate framework | [02-reject-deflection](../banks/hdfc/templates/02-reject-deflection.md) with the new debit in the timeline | gates G0, G2.

---

## Rules for walking the tree

1. **One state, one step.** Never fire two escalations in parallel rungs; never combine a chargeback demand with a rung-skip.
2. **Gates are blocking.** If a named gate fails, use the refusal pattern in [preconditions.md](preconditions.md) — name the gate, the gap, and the path to meet it.
3. **Re-enter at the top after every bank response.** Each reply moves the user to a new state; re-match rather than assuming the old path continues.
4. **The repo stops at S7.** Anything beyond the bank's internal ladder is out of scope in v1.


===== FILE: procedure/classification.md =====

---
title: Classification — picking the correct dispute category
type: procedure
scope: maps a fact pattern to a category; the category decides the applicable rules
last_verified: 2026-06-10
---

# Classification

The single highest-leverage decision in a card dispute is made in the first email: **what category is this?** The category determines which RBI framework applies, which network reason-code family fits, what the deadlines are, and what the bank is obliged to do. Misclassification is silent — the bank will happily process a wrongly-categorised complaint to a dead end.

**Plain-English summaries below are for navigation — verify every rule against the linked regulation entry and its official source before relying on it.** No category implies any particular outcome.

## The first question: did the cardholder authorise *this* debit?

Not "is the charge fair" — **was this specific debit made with the cardholder's authority?**

| | Cardholder authorised this debit | Cardholder did not authorise this debit |
|---|---|---|
| **One-off charge** | Category **C** (service/billing) or **D** (amount error) | Category **A** (unauthorised) |
| **Recurring charge** | C/D — unless the mandate was cancelled or the pre-debit notice was missing → Category **B** | Category **A** (and check B: a never-consented mandate is both) |

## Category A — Unauthorised electronic transaction

**Fact pattern:** the user did not make, authorise, or share credentials for this debit. Card lost/stolen/skimmed, OTP phished, account-takeover, or a debit with no customer action at all.

**Why it matters:** RBI's customer-protection framework on unauthorised electronic transactions governs ([entry](../regulations/rbi/unauthorised-transactions-liability.md)) — it ties the customer's maximum liability to **how quickly the debit is reported**, places the burden of proving customer negligence on the bank, and sets resolution timelines. The clock starts at the user's knowledge of the debit.

**Consequences of choosing A:**
- File immediately; every day of reporting delay can change the liability band.
- The bank's fraud track applies; expect card block/reissue.
- The complaint should say "unauthorised electronic transaction" in those words and cite the entry above — *not* "billing dispute", which routes it away from the liability framework.

**Risk of overusing A:** if the user did authorise the underlying relationship (e.g. signed up, then got charged more than expected), filing it as fraud misroutes the case, can void the better-fitting category-B/C rights, and damages credibility for the rest of the ladder. When in doubt, interview (decision-tree S8).

## Category B — Recurring charge after cancellation / e-mandate non-compliance

**Fact pattern:** a subscription or e-mandate the user once authorised, but: the user cancelled (mandate, subscription, or card-on-file consent) and was charged anyway; or no pre-debit notification arrived as required; or the charge bypassed the mandate framework entirely (e.g. merchant charged a "saved card" directly after mandate cancellation).

**Why it matters:** RBI's e-mandate framework for recurring card transactions ([entry](../regulations/rbi/recurring-payments-emandate.md)) sets the conditions for recurring debits — registration with additional-factor authentication, pre-debit notification, and the right to withdraw the mandate. Separately, the card networks maintain a dispute category specifically for **cancelled recurring transactions** ([Visa](../regulations/networks/visa-reason-codes.md) · [Mastercard](../regulations/networks/mastercard-reason-codes.md) · [RuPay](../regulations/networks/rupay-dispute-rules.md)), which gives the issuing bank a concrete chargeback path.

**Consequences of choosing B:**
- The complaint cites the framework entry *and* names the cancelled-recurring network category — two independent hooks instead of zero.
- Proof of cancellation (or absence of the pre-debit notice) becomes the core evidence; the evidence pack is built around it.
- "Take it up with the merchant" is an incomplete answer here — the network category exists precisely for this pattern (see `banks/<bank>/known-deflections.md`).

**B vs A boundary:** charged *after a valid cancellation* is B (the original relationship was authorised). A mandate the user *never set up at all* is A. State which one in the complaint.

## Category C — Authorised but disputed (service / billing)

**Fact pattern:** the user made or authorised the transaction, but: goods/services not delivered, not as described, cancelled-but-charged (one-off, not mandate), or a promised refund never arrived ("credit not processed").

**Why it matters:** this is primarily a merchant-dispute path. The network reason-code families for "credit not processed" / "services not provided" apply ([networks index](../regulations/networks/)); networks generally expect an attempt to resolve with the merchant first, and the dispute window typically runs from the transaction or expected-delivery date.

**Consequences of choosing C:**
- Rung 0 (written merchant attempt) is usually a real precondition — see gate G1.
- The chargeback window is the binding deadline; track it from day one (gate G3 exception).
- The bank's role is to raise the network dispute correctly, not to adjudicate the service quality itself.

## Category D — Amount error / duplicate / refund-amount mismatch

**Fact pattern:** right merchant, wrong number: double charge, wrong amount captured, currency conversion error, or a refund issued for less than agreed; disputed-charge late fees and interest not reversed after resolution.

**Why it matters:** these are processing-error claims — usually the cleanest evidence (two statement lines, or the agreed figure vs the credited figure) and the most arithmetic-driven asks.

**Consequences of choosing D:**
- The complaint is an itemised reconciliation: what was charged, what should have been, the delta, including consequential fees/interest/GST on fees ([07-amount-correction](../banks/hdfc/templates/07-amount-correction.md)).
- Duplicate/processing-error network codes apply rather than fraud or service codes.

## Stating the classification

The first complaint should carry one sentence of the form:

> "This is a dispute of an **[unauthorised electronic transaction / recurring debit after mandate cancellation / authorised transaction where the service was not provided / processing error]**, and I request it be handled under the applicable framework."

An AI assistant must state the chosen category and its consequence to the user before drafting, and record it — the category must stay consistent across every rung (escalation-ladder rule 3).


===== FILE: procedure/preconditions.md =====

---
title: Preconditions — what must be true before each step
type: procedure
scope: gates for every step in the decision tree and escalation ladder
last_verified: 2026-06-10
---

# Preconditions

Every externally-facing step (anything that sends a complaint or escalation to the bank) is gated. An AI assistant using this repo must check the relevant gate **before** producing a draft, and must refuse — explaining which precondition is unmet and how to meet it — rather than draft around a missing gate. The user being angry, or time feeling short, does not open a gate. (If a *chargeback window* is genuinely closing, that changes which step is urgent — it does not skip a gate; see G3.)

## G0 — Facts captured (gate for everything)

All of the following, from the user, before any draft:

- [ ] The transaction as it appears on the statement: date, merchant descriptor, amount, currency.
- [ ] Card last-4 digits (never the full number — refuse it if offered).
- [ ] What makes it disputed, in one sentence, in the user's words.
- [ ] Any prior contact with bank or merchant: dates, channels, reference numbers, outcomes.
- [ ] Whether the card is still active, and whether the charge is one-off or recurring.

**Unmet →** interview the user (see HOW_AI_SHOULD_USE_THIS.md, interview pattern). Do not proceed on a partial fact set; a draft with holes invites closure on a technicality.

## G1 — Classification done (gate for the first complaint)

- [ ] The dispute has been classified per [classification.md](classification.md) and the classification stated to the user with its consequence.
- [ ] If category A (unauthorised): the user has been told the reporting-delay liability rule and the complaint is being filed **immediately** — this category is time-critical (see [the liability entry](../regulations/rbi/unauthorised-transactions-liability.md)).
- [ ] If category B (cancelled recurring/e-mandate): proof of cancellation (or of the missing pre-debit notification) is identified, even if not yet exported.
- [ ] If category C (service/billing with reachable merchant): one written merchant attempt exists or a stated reason why it would be futile.

**Unmet →** classify first. The category decides the rules, the template, and the deadline math. A wrong category is worse than a late complaint.

## G2 — Reference number captured (gate for every escalation past L1)

- [ ] An L1 complaint exists with a bank-issued **reference number**, captured verbatim.
- [ ] The date it was filed and the SLA stated (or the bank's published L1 SLA) are known.

**Unmet →** file at L1 first, or — if L1 was filed but no reference was given — the next step is a reference-number demand at L1, not an escalation. Higher rungs evaluate "was the rung below exhausted"; without a reference number nothing below is provable.

## G3 — Escalation trigger met (gate for moving up any rung)

One of:

- [ ] The current rung's SLA has lapsed (filed date + `sla_days` from `banks/<bank>/contacts.md` < today), **or**
- [ ] The bank closed/replied with a written outcome that is factually wrong or matches an entry in `banks/<bank>/known-deflections.md` (quote it in the escalation), **or**
- [ ] The bank's reply resolves a different question than the complaint asked (note the mismatch explicitly).

**Unmet →** wait out the SLA while assembling the evidence pack (`templates-shared/evidence-index.md`). Escalating early gives the higher rung a procedural reason to bounce the complaint back down.

**Exception — closing chargeback window:** if the network dispute window (see `regulations/networks/`) would lapse before the current rung's SLA, do not wait silently: the correct step is the [chargeback demand template](../banks/hdfc/templates/03-chargeback-demand.md) at the **current** rung, stating the window date. The window is a reason to act at the rung you are on — never a reason to skip one.

## G4 — Escalation package complete (gate for L3 and above)

- [ ] Timeline table built (`templates-shared/timeline-table.md`) — every event dated, referenced, sourced.
- [ ] Evidence pack indexed (`templates-shared/evidence-index.md`) — numbered, each item named in the index.
- [ ] Every prior reference number and every bank reply (quoted or attached) included.
- [ ] The ask is identical to the original complaint (or the delta is explained, e.g. accrued late fees added with dates).

**Unmet →** build the package first. At PNO level the file is read cold by someone new; the package *is* the case.

## G5 — Internal ladder exhausted (boundary gate — v1 stops here)

- [ ] PNO (or the bank's highest published internal level) responded inadequately or its SLA lapsed, with references and dates in hand.

**Met →** this repo's guidance ends. The RBI Ombudsman route exists ([reference entry](../regulations/rbi/ombudsman-scheme-2021.md)) with its own strict preconditions and time limits; the user should read the scheme at its official source. v1 deliberately does not walk the filing. An AI must say this plainly rather than improvise filing guidance.

---

## Refusal pattern (for the AI)

When a gate is unmet, the refusal must name the gate, the missing item, and the path to meet it:

> "I can't draft the PNO escalation yet: gate G3 isn't met — HDFC's L2 SLA of {{N}} days runs until {{DATE}} and there's no written closure from them. Escalating today gives them a procedural reason to bounce it. While we wait, let's build the evidence index so the escalation is ready to send the day the SLA lapses."


===== FILE: procedure/escalation-ladder.md =====

---
title: Universal escalation ladder (bank-agnostic)
type: procedure
scope: any Indian bank, card disputes
last_verified: 2026-06-10
---

# The universal escalation ladder

Indian bank grievance redressal is a **strict ladder**. Skipping a rung is the most common procedural way to lose a valid dispute: the higher rung (and ultimately the RBI Ombudsman) checks whether the rungs below were exhausted, and bounces complaints that skipped them. Climb in order, document every rung, and only climb when the rung below has actually failed (trigger met).

Bank-specific recipients, addresses, and exact SLAs live in `banks/<bank>/escalation-ladder.md` and `banks/<bank>/contacts.md`. This file defines the universal shape.

> **Parallel clock warning:** card-network chargeback rights run on their **own** clock (typically measured from the transaction or expected-service date — see `regulations/networks/`). The grievance ladder does not pause that clock. If the dispute is chargeback-eligible, the chargeback must be demanded early (rung 1–2), not after the ladder is exhausted.

## Rung 0 — Merchant (conditional)

- **Trigger:** the dispute is about service/goods/billing with a reachable, legitimate merchant (see [classification.md](classification.md), category C/D).
- **Skip when:** the transaction is unauthorised, the merchant is unreachable/abusive, or a cancelled mandate was bypassed — go straight to rung 1.
- **What to do:** one written attempt with a stated deadline; keep the proof. Card networks often expect an attempt-to-resolve-with-merchant for service disputes, and it strengthens every later rung.
- **Do not accept as resolution:** verbal promises without a reference or date.

## Rung 1 — Bank customer service (L1)

- **Trigger:** you have a disputed transaction and your facts captured (gate G1 in [preconditions.md](preconditions.md)).
- **Recipient:** the bank's published card customer-service channel (`banks/<bank>/contacts.md`, level L1).
- **What to include:** the [initial dispute template](../banks/hdfc/templates/01-initial-dispute.md) content — transaction line as it appears on the statement, the category you classified, the specific ask, the evidence index.
- **Non-negotiable output of this rung:** a **complaint reference number**. No reference number = the complaint does not exist for every later rung. Ask for it explicitly; note date, channel, and the agent's stated SLA.
- **Do not accept as resolution:** "we have noted your concern" without a reference; advice to "contact the merchant" when the category does not require it; closure without a written reason.

## Rung 2 — Grievance / escalation desk (L2)

- **Trigger:** L1's stated SLA expired with no resolution, **or** L1 closed the complaint with a reason that is wrong on facts or is a known deflection (`banks/<bank>/known-deflections.md`).
- **Recipient:** level L2 in `banks/<bank>/contacts.md`.
- **What to include:** L1 reference number, the L1 outcome (quote it), why it is inadequate, the timeline table (`templates-shared/timeline-table.md`), the original ask restated.
- **Do not accept as resolution:** a re-send of the L1 reply; a new reference number that resets the clock without addressing the complaint; a partial credit presented as full resolution.

## Rung 3 — Senior grievance / priority redressal (L3, where the bank publishes one)

- **Trigger:** L2 SLA expired or L2 response repeats the deflection.
- **Recipient:** level L3 in `banks/<bank>/contacts.md`.
- **What to include:** everything in rung 2 plus the L2 reference and response; the evidence pack as an indexed attachment (`templates-shared/evidence-index.md`).
- **Do not accept as resolution:** anything not in writing.

## Rung 4 — Principal Nodal Officer (PNO)

- **Trigger:** the rungs below are exhausted (references + expired SLAs in hand) and the complaint is still unresolved or wrongly closed.
- **Recipient:** the PNO in `banks/<bank>/contacts.md`. The PNO is the bank's RBI-facing complaints owner; this is the last internal rung.
- **What to include:** the full, chronological case — every reference number, every bank reply quoted, the timeline table, the indexed evidence pack, the single specific ask, and a clear statement that this is the final internal escalation before regulator-level remedies.
- **Do not accept as resolution:** verbal assurances; "we are looking into it" past the stated SLA; resolution of a *different* complaint than the one made.

## Rung 5 — RBI Ombudsman (out of scope, v1)

The Reserve Bank - Integrated Ombudsman Scheme 2021 exists above the ladder ([reference entry](../regulations/rbi/ombudsman-scheme-2021.md)) and its core precondition is exactly this ladder: the bank must have rejected the complaint or failed to resolve it within the scheme's waiting period, and the filing must be within its time limit. **This repo deliberately does not cover the filing process in v1** — premature or malformed Ombudsman complaints are the top cause of non-maintainability dismissals. When rung 4 is genuinely exhausted, the user should read the scheme document at its official source before doing anything.

---

## Ladder-wide rules

1. **One rung at a time, in writing, with references.** Every email carries the prior reference numbers.
2. **SLA discipline:** note the bank's stated SLA at each rung; escalate when it lapses, not before (the higher rung will ask).
3. **Same complaint, consistent story:** the facts, amount, and ask must be identical at every rung. Changing numbers mid-ladder is how complaints get re-opened as "new" and clocks reset.
4. **Everything that matters, in the email body or an indexed attachment** — not in a phone call. Calls are fine for status checks; they are not evidence.


===== FILE: banks/hdfc/README.md =====

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


===== FILE: banks/hdfc/contacts.md =====

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


===== FILE: banks/hdfc/escalation-ladder.md =====

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


===== FILE: banks/hdfc/known-deflections.md =====

---
title: Known deflections — documented stall patterns and factual counters
bank: hdfc
entries: 6
tone: factual; these are documented patterns with corrective responses, not accusations of bad faith in any individual case
last_verified: 2026-06-10
---

# Known deflections

A *deflection* is a reply that closes or stalls a complaint without addressing it. The catalogue below documents patterns observed in real HDFC credit card disputes, why each is incorrect or incomplete **as a response to the specific situation described**, and the factual counter. Any of these replies may, in a different situation, be perfectly correct — the entries apply only where the stated fact pattern holds.

Counter-template for all entries: [02-reject-deflection.md](templates/02-reject-deflection.md). The counter text below is what goes in its `{{FACT_CORRECTION}}` placeholder, adapted to the user's facts.

---

## D1 — "Please cancel the mandate with the merchant / through the app"

**Applies when:** the user already cancelled the mandate before the disputed debit.

**Why it is incomplete:** it treats an already-performed act as the pending remedy, and leaves the actual complaint — a debit *after* cancellation — unaddressed. Under the RBI e-mandate framework, no further recurring debits are permitted once a mandate is withdrawn ([entry](../../regulations/rbi/recurring-payments-emandate.md), withdrawal clauses).

**Correct response:** state the cancellation date and method, attach the proof, and ask the specific question the reply avoided: *"The mandate was cancelled on {{CANCELLATION_DATE}} (exhibit E2). The debit of {{TRANSACTION_DATE}} post-dates that cancellation. On what basis was it processed?"*

## D2 — "No debit was processed / we find no such transaction"

**Applies when:** the debit appears on the user's statement.

**Why it is incorrect:** the bank's own statement is the bank's own record. A statement line and a "no debit found" reply cannot both be true.

**Correct response:** attach the statement extract, cite the exact line — date, descriptor, amount — and ask for reconciliation: *"The debit appears on my statement dated {{STATEMENT_DATE}} (exhibit E1). Please reconcile your reply with this statement line and confirm the complaint is being investigated against it."*

## D3 — "The merchant charges your saved card directly; no authorisation was needed"

**Applies when:** the charge is recurring and the user had cancelled the mandate/consent (category B).

**Why it is incomplete:** recurring debits on Indian-issued cards must run within the RBI e-mandate framework — registration with additional-factor authentication, pre-debit notification, and a withdrawal right after which further debits must not be processed and stored card details must be deleted ([entry](../../regulations/rbi/recurring-payments-emandate.md)). "Saved card, no authorisation needed" describes the mechanism of the charge; it does not answer its permissibility after cancellation.

**Correct response:** *"Recurring debits on Indian-issued cards are governed by the RBI e-mandate framework [link the entry]. The mandate was withdrawn on {{CANCELLATION_DATE}}. Please state under which provision of that framework this post-withdrawal debit was processed, or treat it accordingly."*

## D4 — "Please block your card first / we can only act after the card is blocked"

**Applies when:** the dispute is category B/C/D — an authorised-relationship dispute, not card compromise.

**Why it is incomplete:** card blocking addresses credential compromise. A cancelled-mandate, service, or amount dispute involves no compromised credential; blocking imposes cost on the user (reissue, re-linking every legitimate mandate) while leaving the complaint untouched. (For genuine category-A fraud, blocking *is* correct — this entry does not apply there.)

**Correct response:** *"This dispute concerns [a debit after mandate cancellation / a billing error], not a compromised card. No credential misuse is alleged. Please proceed with the dispute as classified; if HDFC's process genuinely requires a block for this category, please cite that requirement in writing."*

## D5 — "Re-sending an earlier reply" (same text, new date, sometimes a new reference)

**Applies when:** the re-sent text was already rejected in writing with evidence.

**Why it is incomplete:** repetition does not address the documented rejection. A new reference number for the same complaint can also quietly restart the clock and fragment the record.

**Correct response:** *"Your reply of {{BANK_REPLY_DATE}} is identical in substance to the reply of [earlier date], which I rejected in writing on [date] with evidence (exhibits E…). Please respond to the rejection, not the original complaint. I am treating all correspondence under reference {{CASE_REF}}; please confirm no parallel reference has been opened."* — and the timeline table gains a row for each repetition.

## D6 — "This is between you and the merchant — please resolve it with them"

**Applies when:** the dispute fits a card-network dispute category (cancelled recurring, credit not processed, paid-by-other-means, etc.).

**Why it is incomplete:** for network-eligible disputes the issuing bank is the cardholder's only door into the network's dispute system; the network categories exist precisely because merchant-side resolution failed or is unavailable. Referring the user back to the merchant, without raising or declining the network dispute in writing, is a non-answer for these categories ([Visa](../../regulations/networks/visa-reason-codes.md) · [Mastercard](../../regulations/networks/mastercard-reason-codes.md) · [RuPay](../../regulations/networks/rupay-dispute-rules.md)).

**Correct response:** use [03-chargeback-demand.md](templates/03-chargeback-demand.md) rather than the generic rejection: it names the applicable network category and asks HDFC either to initiate the dispute or to decline it in writing with the specific rule relied on.

---

## Using this catalogue (for the AI)

1. Match the bank's reply to a pattern **and verify the "applies when" condition against the user's facts** — a pattern match without the condition is not a deflection.
2. Quote the bank's reply exactly in the counter (template 02's `{{BANK_REPLY_QUOTE}}`); paraphrases are contestable, quotes are not.
3. One counter per reply. If a reply stacks deflections (e.g. D1 + D4), lead with the one closest to the money and fold the other into the same email's facts.
4. A countered-then-repeated deflection is an escalation trigger (gate G3) — note it as such in the timeline.


===== FILE: banks/hdfc/templates/01-initial-dispute.md =====

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


===== FILE: banks/hdfc/templates/02-reject-deflection.md =====

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


===== FILE: banks/hdfc/templates/03-chargeback-demand.md =====

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


===== FILE: banks/hdfc/templates/04-pno-escalation.md =====

---
title: Escalation to the Principal Nodal Officer
use_when: All rungs below the PNO are exhausted — SLAs lapsed or written closures in hand — and the complaint is unresolved or wrongly closed (decision-tree S3 at the PNO rung).
recipient_level: PNO
prerequisites:
  - Gate G2 — every prior reference number captured verbatim
  - Gate G3 — the rung below has a lapsed SLA or an inadequate written outcome (quotable)
  - Gate G4 — timeline table built; evidence pack indexed and complete; ask unchanged
placeholders:
  - "{{FULL_NAME}} — cardholder name as registered"
  - "{{CARD_LAST4}} — last 4 digits of the card"
  - "{{TRANSACTION_DATE}} — date of the disputed debit"
  - "{{MERCHANT_DESCRIPTOR}} — merchant as on statement"
  - "{{DISPUTED_AMOUNT}} — disputed amount in ₹"
  - "{{DISPUTE_CATEGORY_STATEMENT}} — the same classification sentence used since the first complaint"
  - "{{ALL_CASE_REFS}} — every complaint reference issued so far, each with its filing date"
  - "{{L1_DATE}} — date the first complaint was filed"
  - "{{TOTAL_DAYS_PENDING}} — days from first complaint to this email"
  - "{{ESCALATION_HISTORY}} — 3–6 numbered lines: rung, date, reference, outcome quoted in half a sentence"
  - "{{ONE_SENTENCE_ASK}} — the single specific ask, unchanged from the first complaint"
  - "{{RESPONSE_DEADLINE_DATE}} — date the PNO-level published SLA lapses (from contacts.md sla_days)"
attachments_expected:
  - Full evidence pack with cover sheet (templates-shared/document-cover.md), index, and all exhibits
  - Complete timeline table — every event from first cancellation/transaction to this escalation
escalation_if_ignored: ../escalation-ladder.md rung 5 — internal ladder exhausted (gate G5); this repo's guidance stops there (see procedure/preconditions.md G5)
last_verified: 2026-06-10
---

Subject: Escalation to Principal Nodal Officer — unresolved complaint(s) {{ALL_CASE_REFS}} — card ending {{CARD_LAST4}} — pending {{TOTAL_DAYS_PENDING}} days

Dear Principal Nodal Officer,

I am escalating an unresolved credit card dispute to you as HDFC Bank's Principal Nodal Officer, having exhausted the levels below in HDFC's published grievance redressal process.

**The dispute.** {{DISPUTE_CATEGORY_STATEMENT}} The debit: ₹{{DISPUTED_AMOUNT}} by {{MERCHANT_DESCRIPTOR}} on {{TRANSACTION_DATE}}, on my credit card ending {{CARD_LAST4}}.

**The history.** First complaint filed {{L1_DATE}}; pending {{TOTAL_DAYS_PENDING}} days as of this email. References and outcomes:

{{ESCALATION_HISTORY}}

The full chronology is in the attached timeline table; every statement in it is supported by a numbered exhibit in the attached, indexed evidence pack. My classification and my ask have not changed at any level.

**The ask.** {{ONE_SENTENCE_ASK}}

I request your written response by {{RESPONSE_DEADLINE_DATE}}, per the timeline HDFC publishes for this level. If the complaint remains unresolved or is again closed without addressing the facts of record, I will pursue the remedies available beyond the bank's internal process.

Sincerely,
{{FULL_NAME}}
Card ending {{CARD_LAST4}} · References: {{ALL_CASE_REFS}}

---

> *This draft was prepared with an organisational tool, not by a lawyer. It is not legal advice. Verify all regulatory citations against the linked primary sources and all contact details against the bank's official page before sending. No outcome is predicted or guaranteed.*


===== FILE: banks/hdfc/templates/05-grievance-officer.md =====

---
title: Escalation to the grievance redressal officer (credit cards)
use_when: The L1 rung has failed (lapsed SLA or inadequate written outcome) — HDFC's ladder places its credit-card Grievance Redressal Officer at Level 2, below the PNO (decision-tree S3 at that rung). Check banks/hdfc/escalation-ladder.md for the current rung order.
recipient_level: L2 — Grievance Redressal Officer (credit cards)
prerequisites:
  - Gate G2 — prior reference number(s) captured verbatim
  - Gate G3 — the rung below has a lapsed SLA or an inadequate written outcome (quotable)
  - Gate G4 — timeline table built; evidence pack indexed
placeholders:
  - "{{FULL_NAME}} — cardholder name as registered"
  - "{{CARD_LAST4}} — last 4 digits of the card"
  - "{{TRANSACTION_DATE}} — date of the disputed debit"
  - "{{MERCHANT_DESCRIPTOR}} — merchant as on statement"
  - "{{DISPUTED_AMOUNT}} — disputed amount in ₹"
  - "{{DISPUTE_CATEGORY_STATEMENT}} — the same classification sentence used since the first complaint"
  - "{{ALL_CASE_REFS}} — every complaint reference issued so far, with filing dates"
  - "{{PRIOR_OUTCOME_QUOTE}} — the operative sentence of the most recent bank outcome, quoted exactly"
  - "{{WHY_INADEQUATE}} — one or two sentences: the dated, evidenced fact the outcome fails to address"
  - "{{EXHIBIT_REF}} — evidence index number(s) for that fact"
  - "{{ONE_SENTENCE_ASK}} — the single specific ask, unchanged"
  - "{{RESPONSE_DEADLINE_DATE}} — date this level's published SLA lapses (from contacts.md sla_days)"
attachments_expected:
  - Indexed evidence pack including all bank replies to date
  - Updated timeline table
escalation_if_ignored: 04-pno-escalation.md once gate G3 is met at this rung
last_verified: 2026-06-10
---

Subject: Escalation to Grievance Redressal Officer — unresolved complaint(s) {{ALL_CASE_REFS}} — card ending {{CARD_LAST4}}

Dear Grievance Redressal Officer,

I am escalating an unresolved credit card dispute under HDFC Bank's published grievance redressal process, the prior level having failed to resolve it within its timeline.

**The dispute.** {{DISPUTE_CATEGORY_STATEMENT}} The debit: ₹{{DISPUTED_AMOUNT}} by {{MERCHANT_DESCRIPTOR}} on {{TRANSACTION_DATE}}, on my credit card ending {{CARD_LAST4}}. References to date: {{ALL_CASE_REFS}}.

**Why this escalation.** The most recent response states:

> "{{PRIOR_OUTCOME_QUOTE}}"

{{WHY_INADEQUATE}} (exhibit {{EXHIBIT_REF}}, attached). The complaint therefore stands unresolved on its facts.

The attached timeline table and indexed evidence pack carry the complete record; my classification and ask are unchanged from the first complaint.

**The ask.** {{ONE_SENTENCE_ASK}}

I request your written, substantive response by {{RESPONSE_DEADLINE_DATE}}, per the timeline HDFC publishes for this level. If the matter is not resolved at your level, I will escalate to the Principal Nodal Officer with this correspondence attached.

Sincerely,
{{FULL_NAME}}
Card ending {{CARD_LAST4}} · References: {{ALL_CASE_REFS}}

---

> *This draft was prepared with an organisational tool, not by a lawyer. It is not legal advice. Verify all regulatory citations against the linked primary sources and all contact details against the bank's official page before sending. No outcome is predicted or guaranteed.*


===== FILE: banks/hdfc/templates/06-merchant-representment-rebuttal.md =====

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


===== FILE: banks/hdfc/templates/07-amount-correction.md =====

---
title: Amount correction — partial or incorrect credit
use_when: HDFC has resolved the dispute in principle but the credited amount is wrong — partial refund, or disputed-charge late fees, interest, or GST on fees not reversed (decision-tree S6).
recipient_level: the rung that issued the credit (L1/L2/L3)
prerequisites:
  - Gate G2 — complaint reference captured
  - The credit has actually posted (statement line in hand), so the delta is computable from documents, not estimates
placeholders:
  - "{{FULL_NAME}} — cardholder name as registered"
  - "{{CARD_LAST4}} — last 4 digits of the card"
  - "{{CASE_REF}} — complaint reference, verbatim"
  - "{{TRANSACTION_DATE}} — date of the original disputed debit"
  - "{{MERCHANT_DESCRIPTOR}} — merchant as on statement"
  - "{{DISPUTED_AMOUNT}} — the amount disputed and upheld"
  - "{{CREDIT_DATE}} — date the credit posted"
  - "{{CREDITED_AMOUNT}} — the amount actually credited, exactly as on the statement"
  - "{{ITEMISATION}} — table rows: each missing component (principal shortfall / late fee dated X / interest for cycle Y / GST on fee Z), its amount, and the statement line evidencing it"
  - "{{DELTA_AMOUNT}} — the total still owed: sum of the itemisation"
  - "{{EXHIBIT_REF}} — evidence index number(s) for the statement lines cited"
  - "{{RESPONSE_DEADLINE_DATE}} — date the current rung's published SLA lapses"
attachments_expected:
  - Statement extracts showing the original debit, the credit, and every fee/interest line in the itemisation
  - Updated timeline table
escalation_if_ignored: 02-reject-deflection.md at the next rung per ../escalation-ladder.md, with the itemisation unchanged
last_verified: 2026-06-10
---

Subject: Complaint {{CASE_REF}} — credited amount incorrect — ₹{{DELTA_AMOUNT}} outstanding — card ending {{CARD_LAST4}}

Dear Sir/Madam,

Thank you for the credit of ₹{{CREDITED_AMOUNT}} posted on {{CREDIT_DATE}} against complaint {{CASE_REF}} (debit of ₹{{DISPUTED_AMOUNT}} by {{MERCHANT_DESCRIPTOR}} on {{TRANSACTION_DATE}}, card ending {{CARD_LAST4}}).

The credit does not fully reverse the impact of the disputed debit. The components still outstanding, each evidenced by a statement line (exhibit {{EXHIBIT_REF}}):

{{ITEMISATION}}

**Total outstanding: ₹{{DELTA_AMOUNT}}.**

Since these fees, interest, and tax arose solely from the disputed debit that has now been credited, I request that they be reversed in full, and that the reversal be reflected with appropriate value-dating so that no further interest accrues on them.

Please confirm in writing by {{RESPONSE_DEADLINE_DATE}}: (1) the reversal of each itemised component, or (2) for any component HDFC declines to reverse, the specific written reason, line by line.

Complaint {{CASE_REF}} should remain open until this reconciliation is complete.

Sincerely,
{{FULL_NAME}}
Card ending {{CARD_LAST4}} · Complaint {{CASE_REF}}

---

> *This draft was prepared with an organisational tool, not by a lawyer. It is not legal advice. Verify all regulatory citations against the linked primary sources and all contact details against the bank's official page before sending. No outcome is predicted or guaranteed.*


===== FILE: templates-shared/evidence-index.md =====

---
title: Evidence index — how to assemble a numbered evidence pack
type: shared-template
used_by: every escalation from L2 upward (gate G4 makes it mandatory at L3+)
last_verified: 2026-06-10
---

# The evidence index

An escalation reviewer reads your case **cold**, often with minutes to spend. Loose screenshots make them reconstruct your story; an indexed pack makes them verify it. The difference is usually the difference between "we are looking into it" and a substantive reply. Ordering matters because the index *is* the argument: read top to bottom, it should prove the timeline without a word of commentary.

## Structure

One PDF (or one email with numbered attachments), opened by a cover sheet ([document-cover.md](document-cover.md)), then the index, then exhibits in index order.

```
EVIDENCE INDEX — complaint ref {{CASE_REF}}

E1  Statement extract showing the disputed debit       (statement, {{STATEMENT_DATE}})
E2  Proof of cancellation / mandate withdrawal          ({{CANCELLATION_PROOF_TYPE}}, {{CANCELLATION_DATE}})
E3  Pre-debit notification — or note of its absence     (notification/none, {{NOTIFICATION_DATE_OR_NONE}})
E4  Written merchant contact and reply, if any          (email, {{MERCHANT_CONTACT_DATE}})
E5  Bank complaint acknowledgement with reference no.   (email/SMS, {{L1_DATE}})
E6  Every bank reply since, in date order               (emails, dated)
E7  Timeline table                                      (templates-shared/timeline-table.md)
```

Adapt the list to the category (a category-A pack has no cancellation proof; a category-D pack opens with the two conflicting figures side by side). Keep the numbering continuous and never re-number between rungs — "E2" must mean the same document at L2 and at the PNO.

## Rules

1. **Number everything; reference by number.** The escalation email says "the mandate was cancelled on {{CANCELLATION_DATE}} (E2)" — not "see attached".
2. **One fact per exhibit.** Don't merge five screenshots into one image; the reviewer can't cite half a picture.
3. **Date every exhibit in the index line.** Undated evidence reads as unverifiable.
4. **Redact what the bank doesn't need:** full card number (keep last 4), other transactions on the statement page, third-party personal data. Never redact dates, amounts, or reference numbers in the disputed lines.
5. **Source-label each exhibit:** statement / bank email / merchant email / app screenshot. A screenshot's source and date go in its index line, since the image may not show them.
6. **The pack grows monotonically.** Each rung adds exhibits (new bank replies) at the end; nothing is removed or reordered. The PNO should be able to diff your L2 pack against your PNO pack and see only additions.
7. **Keep originals.** The pack carries extracts; the user keeps complete statements and full email threads in case they're requested.

## Privacy

The pack goes to the bank — not into this repo, not into a fork, not into a public issue. See [DISCLAIMER.md §5](../DISCLAIMER.md).


===== FILE: templates-shared/timeline-table.md =====

---
title: Timeline table — the chronological backbone of any complaint
type: shared-template
used_by: every escalation; exhibit E-last in the evidence pack; pasted inline at L2+
last_verified: 2026-06-10
---

# The timeline table

A dispute is a story about dates: what happened, when, who was told, and who failed to act within what window. The timeline table compresses that story into something a reviewer can verify in thirty seconds. It is the strongest single artifact in an escalation because it converts a complaint ("they ignored me") into a record ("filed {{DATE}}, ref {{REF}}, SLA lapsed {{DATE}}").

## Format

Four columns, strict chronological order, one row per event:

| date | event | reference | source |
|---|---|---|---|
| `YYYY-MM-DD` | one factual sentence | ticket/email ref or `—` | exhibit number (E1…) or channel |

## Synthetic example (illustrative only — every value below is fake)

| date | event | reference | source |
|---|---|---|---|
| 2026-01-05 | E-mandate for {{MERCHANT}} cancelled via bank app; confirmation received | MNDT-XXXX | E2 |
| 2026-02-03 | Debit of ₹{{AMOUNT}} by same merchant appears on statement | — | E1 |
| 2026-02-03 | No pre-debit notification received for this debit | — | E3 |
| 2026-02-04 | Dispute filed with bank phone banking; reference issued | CC-XXXXXXX | E5 |
| 2026-02-18 | Bank reply: "cancel the mandate with the merchant" — mandate already cancelled 2026-01-05 | CC-XXXXXXX | E6 |
| 2026-02-19 | Deflection rejected in writing; cancellation proof re-attached | CC-XXXXXXX | E6 |

## Rules

1. **Facts only, no adjectives.** "Bank reply did not address the cancellation" is a fact; "bank fobbed me off" is not. The table argues by sequence, not by tone.
2. **Every row sourced.** A row that no exhibit or reference supports gets cut — one unsupported row taints the table.
3. **Include the bank's actions, verbatim where short.** Quoted half-sentences from bank replies (with their date and reference) are the table's sharpest rows.
4. **Include non-events when an obligation existed.** "No pre-debit notification received" or "SLA of {{N}} days lapsed with no response" are rows — absence of a required act is an event.
5. **Never backfill from memory.** A date the user can't evidence goes in as approximate and marked (`~2026-01-xx, per user recollection`) or is left out. A provably-wrong date hands the bank the whole table.
6. **One table, append-only.** Same table at every rung, new rows added at the bottom as events occur — identical history every time it's seen.


===== FILE: templates-shared/document-cover.md =====

---
title: Document cover sheet — first page of a submitted PDF
type: shared-template
used_by: any evidence pack or escalation submitted as a PDF (typically L3+ and postal submissions)
last_verified: 2026-06-10
---

# Document cover sheet

When a complaint travels as a PDF (email attachment or printed for post), the first page decides whether it gets routed correctly. The cover sheet states what the document is, who it concerns, and what is being asked — so that whoever opens it can route and act on it without reading page two.

## Format

```
COMPLAINT ESCALATION — {{BANK_NAME}} CREDIT CARD DISPUTE

Complainant      : {{FULL_NAME}}
Card             : credit card ending {{CARD_LAST4}}
Registered mobile: {{REGISTERED_MOBILE}}  (for identification; expect contact here)
Registered email : {{REGISTERED_EMAIL}}

Complaint ref(s) : {{CASE_REF}} (filed {{L1_DATE}}){{ADDITIONAL_REFS}}
Disputed debit   : ₹{{DISPUTED_AMOUNT}} — {{MERCHANT_DESCRIPTOR}} — {{TRANSACTION_DATE}}
Dispute category : {{DISPUTE_CATEGORY}}   (per the first complaint; unchanged)

Addressed to     : {{RECIPIENT_DESK}}, escalation level {{RECIPIENT_LEVEL}}
Date             : {{SUBMISSION_DATE}}

THE ASK
{{ONE_SENTENCE_ASK}}

CONTENTS
1. This cover sheet
2. Escalation letter ({{PAGE_REF_LETTER}})
3. Timeline table ({{PAGE_REF_TIMELINE}})
4. Evidence index ({{PAGE_REF_INDEX}})
5. Exhibits E1–E{{LAST_EXHIBIT_NUMBER}} ({{PAGE_REF_EXHIBITS}})
```

## Rules

1. **The ask is one sentence on page one.** If the recipient reads nothing else, they read what you want and by when.
2. **References verbatim.** The cover sheet is where routing systems look for the case number — typos here orphan the document.
3. **Category restated, never changed.** The cover sheet carries the same classification as the first complaint (escalation-ladder rule 3).
4. **Page numbers in the contents list.** A cited-but-unfindable exhibit is worse than no exhibit.
5. **No narrative on the cover.** The story lives in the letter and the timeline; the cover routes.


===== FILE: regulations/README.md =====

---
title: Regulations index
type: index
scope: every regulation entry in this repo, with what it's for in a dispute
last_verified: 2026-06-10
---

# Regulations

Plain-English **navigation summaries** of the rules that govern Indian credit card disputes — every entry links its official source and carries a `last_verified` date. **No summary here is a substitute for the source document; verify against the source before relying on anything.** Entries follow [regulation.schema.md](../schema/regulation.schema.md); anything that couldn't be confirmed on an official page is marked `UNVERIFIED`, never guessed.

## RBI

| Entry | Use it when |
|---|---|
| [rbi/recurring-payments-emandate.md](rbi/recurring-payments-emandate.md) | A recurring charge hit after mandate cancellation, or without the 24-hour pre-debit notification — the backbone of category-B disputes |
| [rbi/unauthorised-transactions-liability.md](rbi/unauthorised-transactions-liability.md) | A debit the user never authorised (category A) — liability bands tied to reporting speed, burden of proof, resolution timelines |
| [rbi/credit-card-master-direction.md](rbi/credit-card-master-direction.md) | Billing protests (30-day explanation duty), charges on disputed-as-fraud transactions, credit-bureau reporting during a dispute, the grievance machinery itself |
| [rbi/ombudsman-scheme-2021.md](rbi/ombudsman-scheme-2021.md) | **Reference only — filing is out of scope in v1.** What exists above the bank's internal ladder, and its preconditions |

## Card networks

| Entry | Use it when |
|---|---|
| [networks/visa-reason-codes.md](networks/visa-reason-codes.md) | Naming the Visa dispute category in a chargeback demand (template 03) |
| [networks/mastercard-reason-codes.md](networks/mastercard-reason-codes.md) | Same, for Mastercard cards |
| [networks/rupay-dispute-rules.md](networks/rupay-dispute-rules.md) | Same, for RuPay cards — note NPCI publishes less publicly than the international networks |

## Rules for these entries (binding on contributors and on any AI using them)

1. **Cite by linking.** Never assert what a regulation says without linking the entry, which links the source.
2. **The source wins.** A summary that disagrees with its source is a bug — fix the summary.
3. **Clause references, not full text.** These entries map documents; they do not reproduce them.
4. **Old debits, old rules.** A transaction is judged under the instrument in force on its date; entries keep predecessor/amendment tables for exactly this reason.


===== FILE: regulations/rbi/recurring-payments-emandate.md =====

---
title: Digital Payments – E-mandate Framework, 2026 (and predecessor e-mandate circulars)
regulator: RBI
official_reference: RBI/DPSS/2026-27/396; RBI/CO.DPSS.POLC.No.S56/02.14.003/2026-27 (both reference strings appear on the official page)
source_url: https://www.rbi.org.in/Scripts/BS_ViewMasDirections.aspx?id=13374
last_verified: 2026-06-10
applies_to: recurring transactions under e-mandates on Indian-issued cards (and other digital payment instruments), including subscription and standing-instruction debits
plain_english_summary: >
  Recurring card debits in India must run inside RBI's e-mandate framework: the mandate is
  registered with additional-factor authentication (AFA), the issuer must notify the customer at
  least 24 hours before each debit, and the customer can opt out of a single debit or withdraw the
  whole mandate at any time — after which further recurring debits must not be processed. Debits
  above the AFA-exemption limit require fresh authentication. RBI's limited-liability rules for
  unauthorised transactions expressly apply to e-mandate debits.
key_clauses:
  - "Clause 4(a) — one-time mandate registration requires AFA validation"
  - "Clause 4(b) — mandate must state a validity period; issuer must provide a facility to modify or withdraw the mandate at any time"
  - "Clause 4(e) — modification or withdrawal of a mandate requires AFA validation"
  - "Clause 6(a) — pre-transaction notification at least 24 hours before the actual charge/debit"
  - "Clause 6(b) — notification must state: merchant name, amount, date/time of debit, e-mandate reference number, reason for debit"
  - "Clause 6(c) — customer may opt out of a particular transaction or the entire e-mandate on receiving the notification; issuer must act on it (AFA-validated) and confirm"
  - "Clause 6(d) — carve-out: pre-debit notification not required for FASTag/NCMC auto-replenishment mandates"
  - "Clause 7 — post-transaction notification with the same particulars plus grievance redressal details"
  - "Clause 8(a) — AFA-exemption limit ₹15,000 per transaction (general); above it, AFA required"
  - "Clause 8(b) — ₹1,00,000 per transaction limit for insurance premia, mutual fund subscriptions, and credit card bill payments"
  - "Clause 9(a) — issuer must have a dispute/grievance redressal system for e-mandate transactions"
  - "Clause 9(b) — RBI's limited-liability instructions for unauthorised electronic transactions apply to e-mandate recurring transactions"
  - "Clause 10(a) — no charges to the customer for the e-mandate facility"
  - "Clause 11 — repeals the predecessor circulars listed below"
status: verified
---

# RBI e-mandate framework for recurring transactions

**Plain-English summary — verify against the source before relying on this.**

If a merchant debits an Indian-issued card on a recurring basis, that debit is supposed to live inside RBI's e-mandate framework: AFA-validated registration, a pre-debit notification at least 24 hours before each charge (stating merchant, amount, date, reference, and reason), an opt-out on every notification, and an always-available facility to withdraw the mandate — after which further recurring debits must not be processed. The framework also instructs that RBI's limited-liability rules for unauthorised transactions apply to these debits (see [unauthorised-transactions-liability.md](unauthorised-transactions-liability.md)).

Why this matters in a dispute: a recurring debit that arrives **after a mandate withdrawal**, or **without the required pre-debit notification**, is a debit processed outside the framework's conditions — which is the factual basis of a category-B complaint ([classification](../../procedure/classification.md)) and of deflection counters D1/D3 ([known-deflections](../../banks/hdfc/known-deflections.md)).

## Key clauses

See `key_clauses` in the front-matter above; the dispute-critical ones are 4(b)/4(e) (withdrawal right), 6(a)–(c) (pre-debit notification and opt-out), and 9(b) (limited-liability rules apply).

## Predecessor circulars (repealed by clause 11, but governing debits processed while in force)

A debit is judged under the instrument in force on its date. All verified on rbi.org.in, 2026-06-10:

| Instrument | Reference | Date | Source | Dispute-relevant content |
|---|---|---|---|---|
| Processing of e-mandate on cards for recurring transactions | RBI/2019-20/47, DPSS.CO.PD.No.447/02.14.003/2019-20 | 2019-08-21 (effective 2019-09-01) | [rbi.org.in Id=11668](https://www.rbi.org.in/Scripts/NotificationUser.aspx?Id=11668) | The original framework: AFA registration (Annex ¶2), 24-hour pre-debit notification (¶8–9), opt-out (¶10), online withdrawal facility + no debits after withdrawal (¶15–16), merchant must delete card details on withdrawal (¶17), grievance/dispute handling (¶18–19), limited-liability rules apply (¶20). AFA limit ₹2,000 (¶4). |
| UPI extension | RBI/2019-20/139, DPSS.CO.PD No.1324/02.23.001/2019-20 | 2020-01-10 | [Id=11784](https://www.rbi.org.in/Scripts/NotificationUser.aspx?Id=11784) | Extends the framework to UPI, mutatis mutandis. |
| Limit raised to ₹5,000 | RBI/2020-21/74, DPSS.CO.PD No.754/02.14.003/2020-21 | 2020-12-04 (effective 2021-01-01) | [Id=12002](https://www.rbi.org.in/Scripts/NotificationUser.aspx?Id=12002) | Also: non-compliant recurring arrangements "shall not be continued beyond March 31, 2021" (¶3). |
| Compliance deadline extension | RBI/2020-21/118, CO.DPSS.POLC.No.S34/02-14-003/2020-2021 | 2021-03-31 | [Id=12051](https://www.rbi.org.in/Scripts/NotificationUser.aspx?Id=12051) | Final extension to 2021-09-30; no new non-compliant mandates during extension. |
| Limit raised to ₹15,000 | RBI/2022-23/73, CO.DPSS.POLC.No.S-518/02.14.003/2022-23 | 2022-06-16 | [Id=12341](https://www.rbi.org.in/Scripts/NotificationUser.aspx?Id=12341) | AFA-exemption limit ₹5,000 → ₹15,000. |
| ₹1,00,000 for three categories | RBI/2023-2024/88, CO.DPSS.POLC.No.S-882/02.14.003/2023-24 | 2023-12-12 | [Id=12570](https://www.rbi.org.in/Scripts/NotificationUser.aspx?Id=12570) | Higher limit only for mutual funds, insurance premia, credit card bill payments. |
| FASTag/NCMC auto-replenishment | RBI/2024-25/64, CO.DPSS.POLC.No.S528/02-14-003/2024-25 | 2024-08-22 | [Id=12722](https://www.rbi.org.in/Scripts/NotificationUser.aspx?Id=12722) | Brings auto-replenishment under the framework; exempts it from the 24-hour pre-debit notification. |

Also repealed: a "Clarification issued to IBA on e-mandate based recurring transactions" dated 2021-10-08, named in the 2026 framework's repeal table without a circular number. Its standalone URL: `UNVERIFIED` — it appears to have been a clarification letter to the Indian Banks' Association, not a numbered public circular; it is cited here only as listed in the repeal table.

## Related

- The credit-card Master Direction's billing-dispute clauses: [credit-card-master-direction.md](credit-card-master-direction.md)
- Liability when a debit is treated as unauthorised: [unauthorised-transactions-liability.md](unauthorised-transactions-liability.md)
- The network dispute category for cancelled recurring charges: [Visa](../networks/visa-reason-codes.md) · [Mastercard](../networks/mastercard-reason-codes.md) · [RuPay](../networks/rupay-dispute-rules.md)


===== FILE: regulations/rbi/unauthorised-transactions-liability.md =====

---
title: Limiting liability of customers in unauthorised electronic banking transactions (now Chapter IV-D of the Commercial Banks – Responsible Business Conduct Directions, 2025)
regulator: RBI
official_reference: "Current: RBI (Commercial Banks – Responsible Business Conduct) Directions, 2025 — RBI/DOR/2025-26/170, DOR.MCS.REC.No.89/01-01-032/2025-26, dated 2025-11-28, Chapter IV Section D. Origin: circular RBI/2017-18/15, DBR.No.Leg.BC.78/09.07.005/2017-18, dated 2017-07-06"
source_url: https://www.rbi.org.in/Scripts/BS_ViewMasDirections.aspx?id=13140
last_verified: 2026-06-10
applies_to: unauthorised electronic banking transactions on accounts and cards issued by commercial banks (credit cards appear as named categories in the liability table); NBFC-issued cards route here via the NBFC card directions
plain_english_summary: >
  The customer's maximum liability for an unauthorised electronic transaction depends on how
  fast it is reported. Bank's own fault: zero liability regardless. Third-party breach reported
  within 3 working days of the bank's communication: zero liability. Reported on days 4–7: capped
  (₹10,000 for credit cards with limit up to ₹5 lakh; ₹25,000 above that). Beyond 7 working days:
  the bank's board-approved policy applies. The bank must shadow-credit the amount within 10
  working days of notification, resolve within 90 days, and the burden of proving customer
  liability lies on the bank.
key_clauses:
  - "Para 67 — zero liability: bank-side contributory fraud/negligence/deficiency (irrespective of reporting); third-party breach reported within 3 working days of communication from the bank"
  - "Para 68 + Table 1 — third-party breach reported within 4–7 working days: liability is the transaction value or the table cap, whichever is lower; credit cards with limit up to ₹5 lakh: ₹10,000; credit cards with limit above ₹5 lakh: ₹25,000 (other account categories: ₹5,000/₹10,000/₹25,000 per the table)"
  - "Para 69 — reported beyond 7 working days: liability per the bank's board-approved policy (which the bank must publish)"
  - "Para 72 — shadow reversal: the disputed amount credited within 10 working days of customer notification, value-dated to the transaction date"
  - "Para 73 — complaint resolution / liability establishment within board-policy time, not exceeding 90 days from receipt"
  - "Para 75 — burden of proving customer liability lies on the bank"
status: verified
---

# Limiting customer liability for unauthorised electronic transactions

**Plain-English summary — verify against the source before relying on this.**

This is the framework behind every category-A dispute ([classification.md](../../procedure/classification.md)) and the reason gate G1 makes category-A filing **immediate**: the liability bands are keyed to reporting speed — 3 working days for zero liability on third-party breach, days 4–7 for the capped band, board policy beyond that — and the clock runs from the bank's communication of the transaction. Two clauses do quiet work in escalations: the **10-working-day shadow credit** (para 72) and the **bank's burden of proof** (para 75) — a closure that asserts customer negligence without evidence is contestable on the framework's own terms.

## Where the rule lives now (verified chain of custody)

| Instrument | Reference | Date | Source | Status |
|---|---|---|---|---|
| **Current:** RBI (Commercial Banks – Responsible Business Conduct) Directions, 2025, Chapter IV Section D | RBI/DOR/2025-26/170, DOR.MCS.REC.No.89/01-01-032/2025-26 | 2025-11-28 | [rbi.org.in id=13140](https://www.rbi.org.in/Scripts/BS_ViewMasDirections.aspx?id=13140) | verified — paras 67/68/69/72/73/75 and Table 1 confirmed verbatim |
| Origin: Customer Protection – Limiting Liability of Customers in Unauthorised Electronic Banking Transactions | RBI/2017-18/15, DBR.No.Leg.BC.78/09.07.005/2017-18 | 2017-07-06 | [Id=11040](https://www.rbi.org.in/Scripts/NotificationUser.aspx?Id=11040) | verified as to identity and substance; its *internal* paragraph numbering: UNVERIFIED at verbatim level (PDF is bot-protected; substance re-confirmed verbatim in the 2025 Directions) — cite the 2025 paras |
| Consolidation/withdrawal circular (244 Master Directions consolidated) | RBI/2025-26/100, DOR.RRC.REC.302/33-01-010/2025-26 | 2025-11-28 | [Id=13170](https://www.rbi.org.in/scripts/NotificationUser.aspx?Id=13170) | verified |

**Which to cite:** for conduct from 2025-11-28 onward, the 2025 Directions paras above. For older transactions, the 2017 circular governs as the instrument in force at the time (cite it by number and date, by substance rather than internal para number).

## Related instruments (verified)

- **Non-bank PPI issuers:** RBI/2018-19/101, DPSS.CO.PD.No.1417/02.14.006/2018-19, 2019-01-04 — same shape (3 days zero liability; days 4–7 capped at transaction value or ₹10,000; 10-day reversal; 90-day resolution; burden on issuer). [Id=11446](https://www.rbi.org.in/Scripts/NotificationUser.aspx?Id=11446)
- **Co-operative banks:** RBI/2017-18/109, DCBR.BPD.(PCB/RCB).Cir.No.06/12.05.001/2017-18, 2017-12-14 — same framework. [source](https://www.rbi.org.in/commonman/english/scripts/Notification.aspx?Id=2623)
- **NBFC-issued credit cards:** RBI (Non-Banking Financial Companies – Credit Cards: Issuance and Conduct) Directions, 2025 — RBI/DOR/2025-26/348, DOR.AUT.REC.No.267/24-01-041/2025-26, 2025-11-28 — routes cardholder liability to the Commercial Banks RBC Directions above. [id=12956](https://www.rbi.org.in/Scripts/BS_ViewMasDirections.aspx?id=12956)
- **E-mandate debits:** the e-mandate framework states these liability rules apply to recurring transactions processed under it — the bridge between category A and category B ([recurring-payments-emandate.md](recurring-payments-emandate.md)).

## Pending change (not in force)

A draft "Review of Framework of Limiting Customer Liability in Digital Transactions" was issued **2026-03-06** for public comments (closed 2026-04-06), proposing wider fraud coverage, faster timelines, and small-value compensation. **Draft only as of last_verified** — do not cite it as law; check [the press release](https://www.rbi.org.in/Scripts/BS_PressReleaseDisplay.aspx?prid=62340) for its current status.

## Related

- [classification.md](../../procedure/classification.md) — category A and its reporting-speed consequence
- [credit-card-master-direction.md](credit-card-master-direction.md) — the card-conduct rules that cross-refer here
- Network fraud codes for the same fact pattern: [Visa 10.x](../networks/visa-reason-codes.md) · [Mastercard 4837](../networks/mastercard-reason-codes.md)


===== FILE: regulations/rbi/credit-card-master-direction.md =====

---
title: Master Direction – Credit Card and Debit Card – Issuance and Conduct Directions, 2022
regulator: RBI
official_reference: RBI/2022-23/92, DoR.AUT.REC.No.27/24.01.041/2022-23 (consolidated version updated as on 2024-03-07) — REPEALED 2025-11-28; see the Currency section
source_url: https://www.rbi.org.in/Scripts/BS_ViewMasDirections.aspx?id=12300
last_verified: 2026-06-10
applies_to: credit card issuance and conduct by banks and NBFC issuers in India, including billing disputes and grievance redressal — for conduct up to 2025-11-28; successor directions after that date
plain_english_summary: >
  RBI's conduct rulebook for card issuers. For disputes, the load-bearing parts: the issuer must
  explain a protested bill (with documents where applicable) within 30 days; no charges may be
  levied on a transaction the cardholder has disputed as fraud until resolved; a pending dispute
  must not be reported as default to credit bureaus; a grievance mechanism with complaint numbers
  is mandatory; and if the issuer gives no satisfactory response within 30 days, the cardholder
  may approach the RBI Ombudsman.
key_clauses:
  - "Para 10(b) — issuer must not raise wrong bills; on a protested bill, explanation and (where applicable) documentary evidence within a maximum of 30 days from the complaint date"
  - "Para 10(d) — no charges on transactions disputed as 'fraud' by the cardholder until the dispute is resolved"
  - "Para 10(e) — any debit to the card account must follow RBI's prescribed authentication framework (ties e-mandate compliance into billing)"
  - "Para 10(g) — refund/failed/reversed transaction credits before due date must be immediately adjusted and notified"
  - "Para 10(h) — larger refund credits on a paid account: explicit consent to adjust; on request, reversal to bank account within 3 working days"
  - "Para 12(b) — no default reporting to a Credit Information Company while a dispute is pending; status update within 30 days of settlement"
  - "Para 26(a) — grievance redressal mechanism mandatory; grievance redressal officer's contact details on every bill/statement"
  - "Para 26(b) — automatic escalation of unresolved complaints; complaints acknowledged with complaint/docket numbers"
  - "Para 26(c) — issuer liable to compensate for loss/expense/harassment where at fault; no satisfactory response within a maximum of 30 days → cardholder may approach the RBI Ombudsman"
status: verified
---

# Credit Card Master Direction, 2022 — dispute-relevant clauses

**Plain-English summary — verify against the source before relying on this.**

This Master Direction is why several recurring complaints in this repo's templates are phrased the way they are. A protested bill obliges the issuer to explain itself, with documents, within 30 days (¶10(b)). A transaction disputed *as fraud* must not accrue charges while the dispute is open (¶10(d)) — relevant to category-A complaints and to the [amount-correction template](../../banks/hdfc/templates/07-amount-correction.md)'s fee-reversal itemisation. A pending dispute must not be reported as default to credit bureaus (¶12(b)) — worth citing if collections or bureau threats appear mid-dispute. And the grievance machinery this repo's whole ladder walks — complaint numbers (gate G2), a designated grievance redressal officer printed on every statement, the 30-day outer limit after which the Ombudsman route opens — lives in ¶26.

Note: the 30-day non-response window in ¶26(c) is also the practical bridge between this repo's gate G5 (internal ladder exhausted) and the [Ombudsman scheme](ombudsman-scheme-2021.md) — whose filing remains out of scope in v1.

## Key clauses

See `key_clauses` in the front-matter. The consolidated version verified is "Updated as on March 07, 2024" as marked on the official page (which remains online).

## Currency — repealed and replaced on 2025-11-28

As part of RBI's consolidation of 244 Master Directions (withdrawal circular RBI/2025-26/100, DOR.RRC.REC.302/33-01-010/2025-26, dated 2025-11-28 — [verified](https://www.rbi.org.in/scripts/NotificationUser.aspx?Id=13170)), this 2022 Master Direction was repealed. Successors:

- **Commercial banks:** RBI/DOR/2025-26/155, dated 2025-11-28 — [id=13155](https://www.rbi.org.in/Scripts/BS_ViewMasDirections.aspx?id=13155). **Clause mapping UNVERIFIED:** the clause numbers in this entry (10(b), 10(d), 12(b), 26…) are the 2022 text's; whether and where each survives in the successor has not been verified — check the successor before citing clause numbers for conduct after 2025-11-28.
- **NBFC issuers:** RBI (Non-Banking Financial Companies – Credit Cards: Issuance and Conduct) Directions, 2025 — RBI/DOR/2025-26/348, DOR.AUT.REC.No.267/24-01-041/2025-26, dated 2025-11-28 — [id=12956](https://www.rbi.org.in/Scripts/BS_ViewMasDirections.aspx?id=12956), which routes cardholder liability to the [Commercial Banks – Responsible Business Conduct Directions, 2025](unauthorised-transactions-liability.md).

For transactions and bank conduct **while the 2022 MD was in force** (2022-07 to 2025-11), the clause numbers in this entry are the right citations. For later conduct, cite the successor after checking it.

## Related

- E-mandate compliance for recurring debits (¶10(e)'s authentication framework): [recurring-payments-emandate.md](recurring-payments-emandate.md)
- Liability for unauthorised transactions: [unauthorised-transactions-liability.md](unauthorised-transactions-liability.md)
- The Ombudsman scheme this direction points to at the 30-day mark: [ombudsman-scheme-2021.md](ombudsman-scheme-2021.md)


===== FILE: regulations/rbi/ombudsman-scheme-2021.md =====

---
title: Reserve Bank – Integrated Ombudsman Scheme, 2021 (RB-IOS 2021)
regulator: RBI
official_reference: "Notified under s.35A Banking Regulation Act 1949, s.45L RBI Act 1934, s.18 Payment & Settlement Systems Act 2007; launched 2021-11-12; amended by CEPD.PRD.No.S544/13.01.001/2022-23 dated 2022-08-05 (in force 2022-09-01)"
source_url: https://rbidocs.rbi.org.in/rdocs/content/pdfs/RBIOS2021_amendments05082022.pdf
last_verified: 2026-06-10
applies_to: complaints of deficiency in service against RBI-regulated entities (banks, NBFCs, payment system participants), after the entity's own grievance process has been exhausted
plain_english_summary: >
  The Ombudsman is the cost-free forum above the bank's internal ladder — but it only becomes
  available after the bank has been given its chance: a written complaint to the bank first,
  then rejection or 30 days of silence, then filing within the scheme's time limit. A large share
  of Ombudsman complaints are dismissed as non-maintainable for skipping exactly these steps.
  THIS REPO DOES NOT COVER THE FILING (v1 scope) — this entry exists so the preconditions and
  boundary are visible, not as filing guidance. Note: RB-IOS 2021 is replaced by RB-IOS 2026 on
  2026-07-01.
key_clauses:
  - "Clause 10(2)(a) — precondition: a written complaint to the regulated entity first"
  - "Clause 10(2)(a)(i) — and that complaint was rejected wholly/partly, or no reply was received within 30 days of the entity receiving it"
  - "Clause 10(2)(a)(ii) — filing window: within one year of receiving the entity's reply; or, where no reply, within one year and 30 days of the complaint to the entity"
  - "Clause 11(1) — filing channel: the online portal cms.rbi.org.in; physical/email: Centralised Receipt and Processing Centre (CRPC), 4th Floor, RBI, Sector 17, Chandigarh 160017; CRPC@rbi.org.in; toll-free 14448"
  - "Clause 10(1)(a)–(j) — complaints that do not lie: commercial judgment of the entity, outsourcing-contract disputes, grievances not addressed to the Ombudsman, general grievances against management, actions under statutory/law-enforcement orders, services outside RBI's purview, disputes between regulated entities, employment disputes, CICRA-remedy disputes, customers of non-covered entities"
  - "Clause 10(2)(b) — non-maintainable: same cause of action pending/settled before an Ombudsman, court, tribunal, arbitrator or other forum"
  - "Clause 10(2)(c)–(f) — non-maintainable: abusive/frivolous/vexatious; time-barred under the Limitation Act 1963; incomplete information; not lodged by the complainant or authorised representative (advocates barred unless the advocate is the aggrieved person)"
status: verified
---

# RBI Integrated Ombudsman Scheme, 2021 — **reference only**

**Plain-English summary — verify against the source before relying on this.**

> **Scope boundary (v1):** this repo deliberately does not walk the Ombudsman filing — it is the highest-stakes, most procedure-sensitive step, and premature or malformed filings are routinely dismissed as non-maintainable. This entry documents *that the forum exists, what it requires before it will hear a complaint, and where its rules live* — so that the internal ladder (which this repo does cover) is climbed with the Ombudsman's preconditions already satisfied. An AI using this repo must not improvise filing guidance (HOW_AI_SHOULD_USE_THIS, hard prohibitions).

## Why this entry matters *before* you ever reach the Ombudsman

The scheme's preconditions are retrospective judgments on how the bank-level process was run:

- **"Written complaint to the entity first"** — why gate G2 insists on a reference number and written rungs (calls don't count as the written complaint).
- **"Rejected, or 30 days of silence"** — why the timeline table logs filing dates and SLA lapses; the 30-day clock is also published on HDFC's own grievance page as the external-step trigger ([contacts.md](../../banks/hdfc/contacts.md)).
- **"Within one year (or one year + 30 days)"** — why exhausting the internal ladder should not be allowed to drift; the window runs whether or not the bank is responsive.
- **The non-maintainability list (clause 10)** — the documented failure modes this repo's procedure layer is built to avoid.

When gate G5 is met (internal ladder exhausted), the user should read the scheme at the source above and file through the official portal — **cms.rbi.org.in** (verified live at last_verified) — not through any third-party service.

## Currency — read this before relying on the entry

**RB-IOS 2021 stands repealed on 2026-07-01**, replaced by the **Reserve Bank – Integrated Ombudsman Scheme, 2026** (issued via [press release of 2026-01-16](https://www.rbi.org.in/Scripts/BS_PressReleaseDisplay.aspx?prid=62052); repeal-and-saving clause confirmed: complaints, appeals and awards received before that date remain governed by RB-IOS 2021). As of `last_verified` (2026-06-10) **RB-IOS 2021 is the operative scheme** — but any dispute crossing into July 2026 must be checked against RB-IOS 2026, whose preconditions and clause numbers may differ. Re-verify at the source before citing anything in this entry after 2026-07-01.

## Related

- [procedure/preconditions.md](../../procedure/preconditions.md) — gate G5, the boundary where this repo stops
- [procedure/escalation-ladder.md](../../procedure/escalation-ladder.md) — rung 5
- [credit-card-master-direction.md](credit-card-master-direction.md) — the 30-day non-response bridge into the scheme


===== FILE: regulations/networks/visa-reason-codes.md =====

---
title: Visa dispute conditions (Visa Core Rules and Visa Product and Service Rules)
regulator: Visa
official_reference: Visa Core Rules and Visa Product and Service Rules, 18 April 2026 edition, Section 11 (Dispute Resolution) — conditions 11.10.3, 11.10.7, 11.10.8, 11.7.2–11.7.6
source_url: https://usa.visa.com/dam/VCOM/download/about-visa/visa-rules-public.pdf
last_verified: 2026-06-10
applies_to: disputes on Visa-branded cards; the issuing bank files these on the cardholder's behalf
plain_english_summary: >
  Visa's rulebook defines named "dispute conditions" an issuer can file. The ones this repo's
  fact patterns map to: 13.2 Cancelled Recurring Transaction, 13.6 Credit Not Processed,
  13.7 Cancelled Merchandise/Services, and the 10.x Fraud category (10.4 covers unauthorised
  card-absent transactions). Most carry a 120-calendar-day issuer filing window. A cardholder
  cannot file these directly — the issuing bank does — which is why template 03 demands
  initiation or a written refusal.
key_clauses:
  - "Dispute Condition 13.2 — Cancelled Recurring Transaction (rule 11.10.3): permission for a recurring charge was withdrawn (or account closed) before processing, but the charge was billed"
  - "Dispute Condition 13.6 — Credit Not Processed (rule 11.10.7): a credit/void receipt was issued but the credit never processed"
  - "Dispute Condition 13.7 — Cancelled Merchandise/Services (rule 11.10.8): merchandise/services cancelled or returned, still charged"
  - "Dispute Category 10 — Fraud (rules 11.7.2–11.7.6): 10.1/10.2 EMV liability shift, 10.3 other fraud card-present, 10.4 other fraud card-absent (the unauthorised-online-transaction condition), 10.5 fraud monitoring program"
status: verified
---

# Visa dispute conditions

**Plain-English summary — verify against the source before relying on this.**

When a category-B/C/D dispute on a Visa card needs the network route, the issuing bank files under a named **dispute condition**. The cancelled-mandate-still-charged pattern is condition **13.2**; a promised-but-missing refund is **13.6**; cancelled-or-returned-but-charged is **13.7**; a genuinely unauthorised card-absent transaction is category **10.4** (category A in [classification.md](../../procedure/classification.md)). The [chargeback demand template](../../banks/hdfc/templates/03-chargeback-demand.md) uses these names in `{{NETWORK_DISPUTE_CATEGORY}}`.

## Time limits (as stated in the verified edition — these bind the issuer's filing)

- **13.2:** 120 calendar days from the transaction processing date (Table 11-99).
- **13.6:** issuer must wait 15 calendar days from the date on the credit receipt, then dispute within 120 calendar days of that date (if undated, from the cancellation/return date), never beyond 540 calendar days of the transaction processing date (Table 11-125).
- **13.7:** 15-day wait from return/cancellation; 120 calendar days from processing date or from when goods/services were received/expected; 540-day outer cap (Table 11-131).
- **10.1 / 10.4:** 120 calendar days from the transaction processing date (Tables 11-11, 11-29).

Banks set **shorter internal reporting windows** for cardholders than these network limits — the network window is the outer bound, not a reason to wait.

## Two traps worth knowing (both verified in the 2026 edition)

1. **Cancellation must precede the charge for 13.2.** Effective the 18 April 2026 edition, a 13.2 dispute is invalid if the cardholder's cancellation came *after* the transaction date. The cancellation date (exhibit E2) is therefore the load-bearing fact of a category-B Visa dispute.
2. **Fraud and 13.x are mutually exclusive.** A transaction the cardholder calls fraudulent is an *invalid* 13.2/13.6 dispute — it must be filed under 10.x. This is the network-level mirror of the classification rule: category A and category B/C are different tracks, and mixing them voids both.

## Related

- [classification.md](../../procedure/classification.md) — which condition family fits which fact pattern
- [Mastercard equivalents](mastercard-reason-codes.md) · [RuPay](rupay-dispute-rules.md)
- Corroborating official source: Visa, "Dispute Management Guidelines for Visa Merchants" (June 2024), https://usa.visa.com/content/dam/VCOM/global/support-legal/documents/merchants-dispute-management-guidelines.pdf


===== FILE: regulations/networks/mastercard-reason-codes.md =====

---
title: Mastercard chargeback reason codes (Chargeback Guide)
regulator: Mastercard
official_reference: Chargeback Guide, Merchant Edition, 19 May 2026 — Dual Message System reason codes 4853, 4837 (legacy 4841, 4860)
source_url: https://www.mastercard.com/content/dam/mccom/shared/business/support/rules-pdfs/chargeback-guide.pdf
last_verified: 2026-06-10
applies_to: disputes on Mastercard-branded cards; the issuing bank files these on the cardholder's behalf
plain_english_summary: >
  Mastercard consolidates cardholder disputes under reason code 4853 ("Cardholder Dispute"),
  with named sub-conditions including cancelled recurring transactions and refunds not processed.
  Unauthorised transactions go under 4837 ("No Cardholder Authorization") — a separate
  fraud track. The legacy codes 4841 (cancelled recurring) and 4860 (credit not processed) still
  exist but Mastercard recommends 4853. Most filings carry a 120-calendar-day issuer window.
key_clauses:
  - "4853 — Cardholder Dispute: umbrella code; eligible claims explicitly include 'Recurring transaction canceled prior to billing' and 'Refund not processed'"
  - "4853 sub-condition — Cardholder Dispute of a Recurring Transaction: merchant billed after the cardholder cancelled, or cardholder unaware of recurring terms"
  - "4853 sub-condition — Refund Not Processed: merchant agreed to or owed a refund and failed to process it"
  - "4837 — No Cardholder Authorization: cardholder did not authorise the transaction (fraud track; Single Message System equivalent: 37)"
  - "4841 — Canceled Recurring or Digital Goods Transactions: legacy, 'will eventually be eliminated', 4853 recommended"
  - "4860 — Credit Not Processed: legacy, same status, 4853 recommended"
status: verified
---

# Mastercard chargeback reason codes

**Plain-English summary — verify against the source before relying on this.**

On a Mastercard card, the cancelled-mandate-still-charged pattern files under **4853 (Cardholder Dispute)** with the recurring-transaction sub-condition; a missing refund under 4853's refund-not-processed sub-condition; a genuinely unauthorised transaction under **4837** — the fraud track. The [chargeback demand template](../../banks/hdfc/templates/03-chargeback-demand.md) uses these names in `{{NETWORK_DISPUTE_CATEGORY}}`.

## Time limits (as stated in the verified edition — these bind the issuer's filing)

- **4853 recurring-transaction dispute:** within 120 calendar days of the settlement/central-site business date.
- **4853 refund not processed:** between 15 and 120 calendar days from the refund documentation date, cancellation date, or goods-return date (immediate filing allowed on a merchant refund advice or voided receipt).
- **4837:** within 120 calendar days of the central-site business date; not usable for PIN/CDCVM-verified transactions, and capped by Mastercard's Fraud Notification Service rules after repeat fraud chargebacks on the same card number.

Banks set **shorter internal reporting windows** for cardholders than these network limits — treat the network window as the outer bound.

## The classification mirror

The guide states that 4853 *"requires that the cardholder engaged in the transaction"* — fraud claims must go via 4837. This is the same wall as Visa's 13.x/10.x split and this repo's category A vs B/C boundary ([classification.md](../../procedure/classification.md)): pick the wrong side and the filing is invalid on its face.

## Related

- [classification.md](../../procedure/classification.md) — which code fits which fact pattern
- [Visa equivalents](visa-reason-codes.md) · [RuPay](rupay-dispute-rules.md)


===== FILE: regulations/networks/rupay-dispute-rules.md =====

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


===== FILE: examples/hdfc-emandate-bypass/narrative.md =====

---
title: Worked example — e-mandate cancelled, charge processed anyway (narrative)
type: example
status: fully synthetic — every name, amount, date, and reference number below is invented for illustration; resemblance to any real case is incidental
illustrates: category B classification, deflections D1/D2/D3, the chargeback demand, evidence packaging
last_verified: 2026-06-10
---

# Worked example: the e-mandate that wouldn't die

> **This is an illustration, not a precedent.** It shows how the repo's pieces — classification, gates, templates, evidence formats — fit together on one coherent fact pattern. It does not suggest that any step here produces any particular result in another case. All data is synthetic.

## The fact pattern

"R" holds an HDFC credit card ending **4321** (synthetic). In January, R subscribes to a streaming service, **STREAMCO**, on a monthly e-mandate of **₹1,499**.

- **05 Jan** — R cancels the e-mandate through the bank's card-controls app and receives an in-app confirmation (mandate reference `MNDT-0001`, synthetic).
- **03 Feb** — the statement shows a fresh debit: `STREAMCO MUMBAI — ₹1,499` dated 01 Feb. No pre-debit notification was received before it.
- R's first reaction is the common one: complain to the merchant. STREAMCO's support replies that billing "is handled by the payment partner". Dead end.

## Classification (the step that shaped everything after)

Walking [classification.md](../../procedure/classification.md): R *did* authorise the original relationship — so not category A. The charge is recurring, the mandate was cancelled before the debit, and no pre-debit notice arrived — **category B**, on two independent grounds (post-withdrawal debit; missing notification). The complaint will cite the [e-mandate framework entry](../../regulations/rbi/recurring-payments-emandate.md) and name the cancelled-recurring network dispute category.

What classification avoided: filing this as "fraud" (it isn't — the relationship was real, and a fraud filing would have triggered card blocking and the wrong investigation track, per deflection D4's logic), or as a vague "billing complaint" (which loses both the framework hook and the network category).

## The complaint and what came back

- **04 Feb** — Initial dispute filed using [template 01](../../banks/hdfc/templates/01-initial-dispute.md) with the category-B paragraph: cancellation date, method, mandate reference, the missing pre-debit notification, statement extract attached. Reference obtained: `CC-0000001` (synthetic). Gates G0/G1 passed before sending.
- **18 Feb** — Bank reply #1: *"Please cancel the mandate with the merchant to avoid future charges."* — textbook [deflection D1](../../banks/hdfc/known-deflections.md). The mandate was already cancelled, with proof, before the debit.
- **19 Feb** — Deflection rejected using [template 02](../../banks/hdfc/templates/02-reject-deflection.md): cancellation proof re-cited as exhibit E2, the unanswered question asked plainly — *on what basis was a post-withdrawal debit processed?*
- **27 Feb** — Bank reply #2: *"No debit was processed on the mandate, as it stands cancelled."* — [deflection D2](../../banks/hdfc/known-deflections.md) with a twist of D3: technically the *mandate* wasn't debited; the merchant had charged the card-on-file directly, bypassing the cancelled mandate.
- **28 Feb** — Counter filed: the statement line is the bank's own record (E1); the e-mandate framework governs recurring debits regardless of the rail the merchant used, and on withdrawal the merchant was required to delete stored card details. Simultaneously — because "the mandate is cancelled but the charge stands" is exactly the cancelled-recurring pattern — a formal **chargeback demand** went in using [template 03](../../banks/hdfc/templates/03-chargeback-demand.md), naming the network's cancelled-recurring dispute category and noting the dispute window.

## Where it went

The chargeback demand changed the conversation: it asked for a yes-with-date or a no-in-writing-with-rule, neither of which a form reply could supply. The L2 escalation that followed (SLA lapse on the rejection, gate G3 met) attached the complete indexed pack — six exhibits, one timeline table — and the case resolved at that rung with a credit and a fee-reversal follow-up via [template 07](../../banks/hdfc/templates/07-amount-correction.md). *(In this synthetic telling, resolution at L2 is a narrative choice to keep the example short — it is not a representation of how far any real case must or will go.)*

The chronology is in [timeline.md](timeline.md); the transferable lessons are in [what-worked.md](what-worked.md).


===== FILE: examples/hdfc-emandate-bypass/timeline.md =====

---
title: Worked example — timeline table (synthetic)
type: example
status: fully synthetic — all dates, references, and amounts invented for illustration
illustrates: templates-shared/timeline-table.md applied to the narrative in narrative.md
last_verified: 2026-06-10
---

# Timeline table — as it stood at the L2 escalation

> Synthetic illustration of the [timeline-table format](../../templates-shared/timeline-table.md). Note the rows for *non-events* (missing pre-debit notification, lapsed SLA) — absence of a required act is an event. Exhibit numbers refer to the [evidence-index structure](../../templates-shared/evidence-index.md); the synthetic pack is described, not included (no real documents exist).

| date | event | reference | source |
|---|---|---|---|
| 2026-01-05 | E-mandate for STREAMCO cancelled via HDFC card-controls app; in-app confirmation received | MNDT-0001 | E2 |
| 2026-02-01 | Debit of ₹1,499 by STREAMCO MUMBAI processed to card ending 4321 | — | E1 |
| 2026-02-01 | No pre-debit notification received before this debit (required ≥24h prior) | — | E3 (absence noted) |
| 2026-02-02 | Written complaint to STREAMCO support; reply: billing "handled by payment partner" | SC-TKT-9 | E4 |
| 2026-02-04 | Dispute filed with HDFC (template 01, category B); reference issued | CC-0000001 | E5 |
| 2026-02-18 | Bank reply #1: "please cancel the mandate with the merchant" (deflection D1) | CC-0000001 | E6.1 |
| 2026-02-19 | Rejection sent (template 02): cancellation of 2026-01-05 re-evidenced; basis of post-withdrawal debit queried | CC-0000001 | E6.2 |
| 2026-02-27 | Bank reply #2: "no debit was processed on the mandate, as it stands cancelled" (deflections D2/D3) | CC-0000001 | E6.3 |
| 2026-02-28 | Counter sent: statement line cited (E1); e-mandate framework cited via repo entry; merchant card-on-file bypass named | CC-0000001 | E6.4 |
| 2026-02-28 | Formal chargeback demand sent (template 03): cancelled-recurring network category named, window noted | CC-0000001 | E6.5 |
| 2026-03-14 | L1 SLA on the 2026-02-28 counters lapsed with no substantive reply | CC-0000001 | timeline arithmetic |
| 2026-03-16 | L2 escalation sent with cover sheet, this table, and indexed pack E1–E6 (gates G2/G3/G4 checked) | CC-0000001 | E7 |

## What this table is doing (format notes)

1. **Every row is sourced** — to an exhibit, a reference, or explicit arithmetic. No row relies on recollection.
2. **The bank's own words appear as dated rows**, quoted in half-sentences — the two deflections are the two sharpest rows in the table.
3. **Append-only:** rows 1–10 were identical in every email from 2026-02-28 onward; later rungs only ever saw additions.
4. **The non-event rows** (missing notification, lapsed SLA) are what convert "they ignored me" into a record.


===== FILE: examples/hdfc-emandate-bypass/what-worked.md =====

---
title: Worked example — what this example illustrates
type: example
status: fully synthetic — illustrative only; nothing here predicts or implies any outcome in any other case
illustrates: the transferable mechanics, separated from the one-off facts
last_verified: 2026-06-10
---

# What this example illustrates

> Framing matters: this page lists the **mechanics the example was built to show** — not "tactics that win disputes". Whether any dispute resolves, and at what rung, depends on its own facts and the bank's assessment. This repo predicts no outcomes.

## 1. Classification did the heavy lifting before any email was sent

The single decision with the most downstream effect was naming the dispute correctly: **category B, on two independent grounds** (post-withdrawal debit; missing pre-debit notification). Every later email inherited that frame — same sentence, every rung (escalation-ladder rule 3). The two tempting misclassifications — "fraud" and generic "billing complaint" — would each have routed the case onto a track that didn't fit its facts.

## 2. Deflections were answered with the question they avoided

Both form replies were met the same way: quote the reply verbatim, state the dated fact it skipped (with exhibit number), and re-ask the one question it left unanswered. No adjectives, no escalation of tone — escalation of *specificity*. The catalogue in [known-deflections.md](../../banks/hdfc/known-deflections.md) exists so the second person facing "please cancel the mandate" doesn't have to compose the counter from scratch.

## 3. The chargeback demand changed the shape of the conversation

Until [template 03](../../banks/hdfc/templates/03-chargeback-demand.md) went in, every exchange was open-ended — a complaint that could be "noted" indefinitely. The demand was binary: *initiate the network dispute (with date and category), or decline it in writing citing the rule.* Requests that can only be answered with a commitment or a citable refusal are harder to absorb into form-reply loops. The same shape appears in every template's "one clear ask with a deadline" rule.

## 4. The evidence pack was built before it was needed

The pack (E1–E6) and the timeline table were assembled during the *waiting* periods (decision-tree S1 — "wait the SLA out; build the package"), not scrambled together on escalation day. So when gate G3 opened, the L2 escalation went out the same week with the complete record attached — and the L2 reviewer never had to take the complainant's word for anything: every sentence resolved to a numbered exhibit.

## 5. Order was preserved even when it was tempting to skip

After the second deflection, jumping straight to the PNO felt natural. The gates said no: G3 had just been met *for one rung*, not three. The case escalated one level with the record of two countered deflections — which is exactly the record a higher rung needs to see. A skipped rung would have offered a clean procedural reason to bounce the complaint downward and restart the clock.

## 6. The clocks were tracked separately

Two clocks ran at once: the bank's grievance SLA (rung by rung) and the network's dispute window (one-shot, from the transaction date). The chargeback demand went in **while** the L1 exchange was still alive precisely because the window clock doesn't pause for the ladder (gate G3 exception). Conflating the two is one of the failure modes in the BRD's problem statement — and it's invisible until it's too late.

---

*The fact pattern, dates, and resolution rung in this example are synthetic narrative choices. Read it for the mechanics; bring your own facts.*


===== FILE: schema/bank.schema.md =====

---
title: Bank folder schema
type: schema
defines: required structure for any banks/<bank>/ folder
last_verified: 2026-06-10
---

# bank.schema — required structure for a bank folder

Every folder under `banks/` must be **self-contained**: an AI assistant given only `procedure/`, `regulations/`, `templates-shared/`, and one bank folder must be able to run a full dispute for that bank. `banks/hdfc/` is the reference implementation — copy it to start a new bank.

## Folder name

Lowercase, hyphenated, recognisable: `hdfc`, `icici`, `axis`, `sbi-card`.

## Required files

| File | Purpose | Schema it must follow |
|---|---|---|
| `README.md` | Bank overview: which products are covered, quirks (e.g. multiple email domains), folder map | front-matter: `title`, `bank`, `products_covered`, `last_verified` |
| `contacts.md` | Every escalation contact, dated and source-linked | [contact.schema.md](contact.schema.md) per entry |
| `escalation-ladder.md` | The bank's specific rung-by-rung ladder, each rung referencing `contacts.md` and a template | front-matter: `title`, `bank`, `levels` (ordered list), `last_verified` |
| `known-deflections.md` | Documented stall patterns + factual counters, each linked to a template | front-matter: `title`, `bank`, `entries` (count); per entry: `deflection`, `why_incomplete`, `correct_response`, `template` |
| `templates/` | Numbered templates, `NN-purpose.md`, ordered by typical escalation sequence | each file follows [template.schema.md](template.schema.md) |

## Rules

- **Numbering:** templates are `01-…` through `NN-…` in rough escalation order, so an AI can infer sequence from filenames alone.
- **No bank-agnostic logic here.** Universal procedure (category classification, precondition logic, the abstract ladder) lives in `procedure/`. A bank folder holds only what is specific to that bank: contacts, its concrete ladder, its observed deflections, its addressed templates.
- **Self-containment over DRY:** it is acceptable for a bank's escalation-ladder to restate rung descriptions that resemble the universal ladder — an AI may load only the bank folder plus `procedure/`, and a contributor copying the folder needs the full picture in place.
- **Everything dated:** any factual claim about the bank (an SLA, a contact, a portal URL) carries `last_verified` and `source_url` exactly as [contact.schema.md](contact.schema.md) requires.

## Copy-paste starting point

```
banks/<bank>/
├── README.md
├── contacts.md            # re-source every entry from <bank>'s official pages
├── escalation-ladder.md   # rebuild from <bank>'s published grievance levels
├── known-deflections.md   # start empty-ish; grow from documented cases
└── templates/
    ├── 01-initial-dispute.md
    ├── 02-reject-deflection.md
    ├── 03-chargeback-demand.md
    ├── 04-pno-escalation.md
    ├── 05-grievance-officer.md
    ├── 06-merchant-representment-rebuttal.md
    └── 07-amount-correction.md
```


===== FILE: schema/contact.schema.md =====

---
title: Contact entry schema
type: schema
defines: required fields for every contact entry in any banks/<bank>/contacts.md
last_verified: 2026-06-10
---

# contact.schema — required fields for a contact entry

Contacts are **perishable data**. The schema exists so that an AI can always tell a user *how fresh* a contact is and *where to re-check it*. A contact without `last_verified` and `source_url` must not be committed.

## Fields (all required unless marked optional)

| Field | Format | Rule |
|---|---|---|
| `level` | `L1` / `L2` / `L3` / `L4` / `PNO` / `Grievance Officer` | The rung this contact serves. Must match a rung in the bank's `escalation-ladder.md`. |
| `name_or_desk` | free text | Officer name if the bank publishes one, else the desk title (e.g. "Grievance Redressal Cell"). Use `NOT_PUBLISHED` if the bank shows no name — never substitute a name from elsewhere. |
| `email` | exact string from source | Captured character-for-character from the official page (banks use multiple domains). `NOT_PUBLISHED` if none listed. |
| `phone` | exact string from source | Include IVR notes if the page gives them. `NOT_PUBLISHED` if none. |
| `postal_address` | exact string from source | Required for PNO/grievance levels (written escalations may need post). `NOT_PUBLISHED` if none. |
| `escalation_trigger` | one sentence | When a user should use this level, as the bank's page describes it (e.g. "if not resolved at L1 within X days"). |
| `sla_days` | integer or `NOT_PUBLISHED` | The response/resolution time the bank itself states for this level. Never infer one. |
| `source_url` | official bank domain URL | The exact page the values above were read from. One URL per entry; if fields came from different pages, note which. |
| `last_verified` | `YYYY-MM-DD` | The date a human or agent actually loaded `source_url` and saw these values. |
| `notes` | free text (optional) | Quirks: alternate domains, web-form-only levels, "page shows last-updated date of …". |

## Sentinel values

- `NOT_PUBLISHED` — the official source does not list this field. Honest absence.
- `UNVERIFIED` — a value exists in circulation but could not be confirmed on an official page at `last_verified` date. Must carry a `notes` explanation. An AI surfacing an `UNVERIFIED` value must say so to the user.

## Entry format

Entries are markdown sections so humans can read them, with a fenced YAML block so machines can parse them:

```yaml
level: PNO
name_or_desk: Principal Nodal Officer
email: pnohdfcbank@hdfcbank.com   # exact string from source page
phone: "044-23625600"
postal_address: |
  HDFC Bank Ltd. ...
escalation_trigger: Complaint not resolved to satisfaction within 10 days at the grievance cell
sla_days: 10
source_url: https://www.hdfcbank.com/personal/need-help/grievance-redressal
last_verified: 2026-06-10
notes: Example block — values here are illustrative of FORMAT only; real values live in banks/<bank>/contacts.md
```

## Verification rule (restated from CONTRIBUTING.md because it matters most here)

`last_verified` means *"I loaded `source_url` on this date and these values were on it."* It does not mean "this was true when I last used it" or "a blog said so". When re-verifying, if values still match, bump the date; if they changed, change the values **and** the date.


===== FILE: schema/template.schema.md =====

---
title: Template schema
type: schema
defines: required front-matter and body rules for every file in banks/<bank>/templates/
last_verified: 2026-06-10
---

# template.schema — required structure for a template

A template is a ready-to-fill email or letter. The front-matter tells an AI **when** to use it, **what must already be true**, and **exactly which values it must collect from the user**. The body is the text itself with `{{PLACEHOLDER}}` tokens.

## Front-matter fields (all required)

| Field | Format | Rule |
|---|---|---|
| `title` | short name | e.g. "Initial dispute — credit card transaction" |
| `use_when` | one or two sentences | The user situation this template addresses. Must correspond to at least one outcome in `procedure/decision-tree.md`. |
| `recipient_level` | a `level` from contact.schema | Which contacts.md entry receives this. The AI pulls the live address from contacts.md — templates never hardcode an email address. |
| `prerequisites` | list | What must already have happened (mirrors `procedure/preconditions.md` gates). The AI must confirm each before producing the draft. |
| `placeholders` | list of `{{UPPER_SNAKE}}` tokens | **Every** token used in the body, each with a one-line description of what to ask the user. |
| `attachments_expected` | list | What the user should attach (point at `templates-shared/evidence-index.md` formats). |
| `escalation_if_ignored` | path | Which template/rung comes next if this one gets no adequate response within the SLA. |
| `last_verified` | `YYYY-MM-DD` | Date the template's procedural assumptions (recipient level, SLA references) were last checked. |

## Body rules

1. **Placeholders only, no real data.** Tokens are `{{UPPER_SNAKE}}`. Anything that varies per user — names, amounts, dates, reference numbers, card last-4 — is a token. No plausible-looking example values in the body.
2. **Every token declared.** A token in the body that is missing from `placeholders` is a schema violation (it would let an AI fill something undocumented).
3. **Factual tone.** State facts, dates, reference numbers, and the specific ask. No threats, no sarcasm, no adjectives doing argument's work. The strongest sentence in an escalation email is a dated fact the bank already has on record.
4. **Cite by pointer.** Where the body references a regulation, it links the entry in `regulations/` (which links the official source). The body never asserts regulatory content without that pointer.
5. **One clear ask.** Each template ends its body with a single, specific, deadline-carrying request (e.g. resolution reference number, chargeback initiation confirmation, written closure reason).
6. **Disclaimer block.** Every submission-bound template ends with the canonical short-form disclaimer from [DISCLAIMER.md](../DISCLAIMER.md), exactly:

> *This draft was prepared with an organisational tool, not by a lawyer. It is not legal advice. Verify all regulatory citations against the linked primary sources and all contact details against the bank's official page before sending. No outcome is predicted or guaranteed.*

(The block is for the **user's review stage**; the user may remove it from the final sent email — that is their call, made knowingly.)

## Skeleton

```markdown
---
title:
use_when:
recipient_level:
prerequisites:
  -
placeholders:
  - "{{EXAMPLE_TOKEN}} — what to ask the user"
attachments_expected:
  -
escalation_if_ignored:
last_verified:
---

Subject: …{{TOKENS}}…

Body paragraphs with {{TOKENS}}.

One clear ask with a deadline.

[short-form disclaimer block]
```


===== FILE: schema/regulation.schema.md =====

---
title: Regulation entry schema
type: schema
defines: required fields for every file under regulations/
last_verified: 2026-06-10
---

# regulation.schema — required fields for a regulation entry

A regulation entry is a **pointer with a map**, not a copy of the law. It exists so an AI can (a) find the right official document fast, (b) cite it by clause, and (c) never assert regulatory content without a link. The plain-English summary is for navigation only.

## Front-matter fields (all required)

| Field | Format | Rule |
|---|---|---|
| `title` | official document title | As the regulator publishes it. |
| `regulator` | `RBI` / `Visa` / `Mastercard` / `RuPay (NPCI)` | Who issued it. |
| `official_reference` | circular/direction/rule number | Exactly as printed on the document. `UNVERIFIED` if it could not be confirmed on an official page. |
| `source_url` | official-domain URL | rbi.org.in, visa.com, mastercard.com/.us, npci.org.in only. The page or PDF the entry was verified against. |
| `last_verified` | `YYYY-MM-DD` | Date `source_url` was actually loaded and checked. |
| `applies_to` | one line | e.g. "recurring card transactions on Indian-issued cards". |
| `plain_english_summary` | 2–4 sentences | Navigation summary. The body must label it (see below). |
| `key_clauses` | list | `clause ref — one-line description`, one per clause that matters for disputes. |
| `status` | `verified` / `UNVERIFIED` | Whether `official_reference` + clauses were confirmed against `source_url`. |

## Body rules

1. The body opens with this bold line, verbatim, immediately after the heading:
   **Plain-English summary — verify against the source before relying on this.**
2. **No full-text reproduction.** Clause references and one-line descriptions only. Link the official document; the reader reads the law there. (Short phrases needed to identify a clause are fine; paragraphs are not.)
3. **No advice framing.** Entries describe what a rule covers and where it lives — they do not tell a user what they are entitled to in their specific case, and they never predict outcomes.
4. **Unverified means flagged.** If any number, date, or clause could not be confirmed on the official source, mark it `UNVERIFIED` inline and in `status`, with a note on what was checked. A wrong-but-confident citation is the single most damaging error this repo can ship — it hands the bank a reason to dismiss the complaint.
5. **Amendments tracked in place.** If a circular was amended (e.g. limits raised), the entry lists each amendment with its own `official_reference` + `source_url` + date, newest clearly marked as current.

## Skeleton

```markdown
---
title:
regulator:
official_reference:
source_url:
last_verified:
applies_to:
plain_english_summary: >
  …
key_clauses:
  - "clause ref — one-line description"
status: verified
---

# <title>

**Plain-English summary — verify against the source before relying on this.**

<the 2–4 sentence summary, expanded only as far as navigation requires>

## Key clauses
…

## Amendments (if any)
…
```


===== FILE: CONTRIBUTING.md =====

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
