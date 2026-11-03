# Trade-off resolver example: auto-archive or ask first?

## Prompt

> Our AI inbox assistant can classify incoming email as "low priority." Should it auto-archive those emails, or show a suggestion the user has to approve? Users say they want less inbox noise, but a couple of beta users complained they missed an important email.

## Response

```
## Decision: Auto-archive low-priority email, or suggest and wait for approval?
Tension: Effortless Where Possible vs. Forgiving and Controllable (Appropriate Autonomy)

1. User goal: a quieter inbox without missing anything that matters. The second half is the
   real goal; noise reduction serves it.
2. Consequences: a wrongly archived email can mean a missed deadline, client, or payment.
   Low frequency, high cost.
3. Reversibility: technically reversible, since the email is still in the archive. In practice
   it isn't, because the user doesn't know it's there to recover.
4. User and context: busy professionals who scan quickly and won't audit an archive folder.
5. Evidence: two beta complaints about missed email (Observed). Misclassification rate
   unknown (Needs testing).

Call: auto-archive, but put the archived email in a once-a-day "Archived for you" digest
with one-tap restore. Each restore also teaches the classifier. Switch to suggest-and-approve
for any sender the user has replied to in the last 90 days.
Reverse it if: more than ~2% of archived emails are restored, or missed-email complaints
continue after the digest ships.

How we'll know: restore rate from the digest, and complaints about missed email per 1,000
users. Treat a low restore rate carefully: it could mean the classifier is accurate, or that
users aren't reading the digest. Check the digest open rate alongside it.
```

## Why this is a good response

- Names the two principles in tension instead of using one as a slogan
- Spots that "reversible in theory" isn't reversible in practice if users can't find what was archived
- Makes a specific call, with a guardrail for the riskiest case
- States the condition that would reverse the decision
- Treats AI signals as diagnostic: a low restore rate is ambiguous until you check digest opens
