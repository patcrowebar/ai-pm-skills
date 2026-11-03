# Review example: the results come back, and the PM wants a yes

Continues from the [plan example](plan-example.md), in the same chat.

## Prompt

> Okay, we ran it. We talked to 6 customers. 5 said the auto-drafted report would save their team a lot of time and they'd definitely use it. On price, 2 said $25K seemed reasonable, 3 said it should be included in their current license, and 1 didn't answer. Only 1 could name who would approve the spend, and that person said it would need procurement review. Honestly I think this is a pass. 5 of 6 want it, so I want to put it on the Q1 roadmap as a paid add-on. Do you agree?

## Response

I don't agree. Against the bar we set beforehand, this is a **fail on the add-on question**. The feature itself still looks worth pursuing.

```
DECISION AT STAKE
Fund a production build in Q1 as a ~$25K/yr add-on.

EXPECTED
"At least 3 customers, including at least 1 non-requester, name a budget owner who
agrees to a pricing follow-up at $25K, AND their teams would keep most of their draft."
Reconsider if: "most say this should be included, or nobody can name a budget owner."

OBSERVED
5 of 6 said it would save time and they'd use it. On price: 2 reasonable, 3 "should be
included," 1 no answer. 1 named budget owner, with procurement review ahead.
Not captured: how much of each draft customers would keep. Half the planned
evidence is missing.

ASSESSMENT  FAIL on viability: 1 named owner against a bar of 3, and the reconsider
trigger fired, with half the sample asking for it to be included.

THRESHOLD NOTE
The bar was reasonable for 3 weeks. A looser bar wouldn't change the reading either:
3 of 6 said "include it," which points the same way.

WHAT WE LEARNED
  Stronger: the problem is real and the value lands (says only).
  Weaker: charging for it as a separate $25K line item (says: half asked for it to
  be included).
  Still unresolved: draft quality on real data (not captured); whether the one named
  owner turns into a purchase.

RECOMMENDED NEXT DECISION  Change (my recommendation, your call)
Keep it on the roadmap, but drop "paid add-on" as the plan of record. Treat the
packaging as open: retention, a higher tier, or a price increase at renewal.
The initiative kill criteria didn't fire.

NEXT MOVE
Take the one named owner to a real quote before planning locks, and re-run the drafts
to measure how much customers keep. A signature gives you one real commitment. A
procurement stall shows you what selling it as an add-on will look like at scale.
```

"5 of 6 want it" counts interest. Interest was never the open question, since the QBR requests had already shown it. This test was built to measure willingness to pay, and on that, most of the room said "include it."

## Why this is a good response

- Grades against the original threshold, not the user's new framing
- Disagrees directly when asked to agree
- Names evidence that was planned but never captured, instead of grading only what's there
- Checks the threshold itself (THRESHOLD NOTE) without using it to soften the grade
- Tags each finding with its evidence rung
- Recommends "Change," not "Kill," because the initiative kill criteria didn't fire
