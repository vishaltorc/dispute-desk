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
