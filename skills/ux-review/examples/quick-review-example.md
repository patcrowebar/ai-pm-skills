# Quick review example: a checkout screen

## Prompt

> Quick gut check on our checkout screen for a meal-kit subscription. It shows: 3 meals × $11.99 = $35.97, shipping $6.99, total $44.95. Big orange "Complete Order" button at the bottom. If payment fails, we show "Error 402." There's no way to edit the meals from this screen; you have to go back two steps. Anything jump out?

## Response

```
## Quick UX Review: Meal-kit checkout
User: a returning subscriber · Outcome: pay the right amount for the right meals · Stakes: money and trust

Verdict: The layout is clear, but the total doesn't add up and a failed payment leaves people
stuck. Both hit trust at the moment money changes hands.

Top 3 fixes
1. The total doesn't reconcile → $35.97 + $6.99 = $42.96, but the screen shows $44.95. That's a
   $1.99 gap. If it's tax or a fee, show it as its own line. · Trustworthy and Inclusive, Clear
   · Impact: High (Observed; the cause is Assumed)
2. "Error 402" → say what happened and what to do next in plain words, e.g. "Your card was
   declined. Try another card, or check with your bank," and keep the order intact. · Forgiving
   and Controllable · Impact: High
3. No meal editing at checkout → add an inline "Edit meals" link that returns here with the
   cart preserved. · Effortless Where Possible, Contextual and Continuous · Impact: Medium

Keep: the single, clear primary action. Don't add a confirmation dialog on top of it; the
order summary already does that job.

Test it: ask 5 subscribers to check out and say the total out loud before tapping. Count how
many notice the $1.99 gap.
```

Want the Full review? This flow handles money, so it's worth one before launch.

## Why this is a good response

- Does the arithmetic and shows the mismatch, rather than just saying "looks off"
- Ties each fix to a named principle and rates its impact
- Labels what's Observed and what's Assumed
- Protects what's working ("Keep"), and steers away from adding a needless confirmation dialog
- Ends with a cheap test with real users
