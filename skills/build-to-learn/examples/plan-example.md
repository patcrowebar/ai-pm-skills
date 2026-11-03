# Plan example: an enterprise AI feature request

## Prompt

> I'm VP of Product at a B2B compliance software company. Three of our largest enterprise customers asked in QBRs for an AI feature that auto-drafts audit reports from their existing control data. Our engineers think they can build a working prototype in about two weeks. Leadership wants it on the Q1 roadmap, and sales thinks we could charge around $25K per year per customer as an add-on. I have about 3 weeks before Q1 planning locks, access to 6–8 customer contacts, and one engineer part-time. Help me figure out what to do.

## Response

I'm reading the decision as: **do we commit Q1 capacity to a production AI audit-report drafter sold as a ~$25K/yr add-on?** Correct me if the real question is narrower.

```
DECISION AT STAKE
Fund a production build in Q1 as a paid add-on, or not.

RISKIEST BELIEF  [Viability]
Customers who asked will pay ~$25K/yr for it as a separate line item. Feasibility
looks like the obvious risk, but a prototype only proves it runs. Three QBR requests
show a real problem; they don't show anyone will pay, and enterprise AI requests often
carry an unspoken "include it in what we pay." The two-week prototype is the
comfortable test: it would pass and leave the pricing question unanswered.

RECOMMENDED TEST
Concierge drafts plus a real pricing conversation. Week 1: the engineer hand-runs the
model on 2–3 customers' real data and produces one draft each (a script, not product
code). Weeks 2–3: 6–8 sessions with requesters and non-requesters. Show each customer
their own draft, record what they'd keep, then quote a real price and ask who owns the
budget. This tests the belief that can sink the add-on, and checks draft quality on
real data along the way.
Evidence rung: Does (edits to their own draft) → Commits (named budget owner who
agrees to a pricing follow-up). Signed LOIs are unlikely within 3 weeks, so this test
doesn't target them.

EXPECTED EVIDENCE   (your call to adjust)
✓ Continue if: at least 3 customers, including at least 1 non-requester, name a
  budget owner who agrees to a pricing follow-up at $25K, AND their teams would keep
  most of their draft.
✗ Reconsider if: most say "this should be included," or nobody can name a budget owner.
? Inconclusive if: enthusiasm and "the price seems fine in principle," but no named
  owner. In enterprise that's still "says."
Capture: % of each draft kept, exact reaction to the price, owner and buying path,
  any procurement or AI-governance blockers.
Initiative kill criteria (separate from this test): drafts aren't useful on real data,
  AND customers won't fund it even bundled. Failing on price alone means changing the
  packaging, not killing the feature.

EXECUTION
You + one part-time engineer · concierge drafts + pricing sessions · ~3 weeks ·
stop early if the first 3 requesters all say "should be bundled."

EVIDENCE LIMITS
A pass supports: funding a production build with real buyers lined up.
A pass does NOT establish: that deals clear security or procurement, that $25K holds
across the wider customer base, or that customers keep using it after the first cycle.

BRING THIS BACK
Still in this chat? Just tell me what happened. Starting a new chat? Paste this card
first, then the results.
```

**What to tell leadership now:** frame Q1 as "production build, gated on budget-owner commitments by planning lock." That turns the roadmap ask into a decision this test can actually inform.

## Why this is a good response

- Infers the decision instead of running an intake form
- Picks viability over the obvious feasibility risk, and explains why
- Names the comfortable test (the prototype) and steers away from it
- Keeps the pass bar to 2 conditions and targets an evidence rung reachable in 3 weeks
- Keeps the user's $25K price rather than silently changing it
- Separates "change the packaging" from "kill the feature"
