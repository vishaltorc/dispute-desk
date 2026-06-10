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
