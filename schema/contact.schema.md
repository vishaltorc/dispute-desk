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
