# build-to-learn

**A decision-first experiment coach for product bets.**

AI made building cheap. That makes validation cheap too, so the bar should go up, not down. build-to-learn helps you work out what you actually need to learn before committing time or money, then tells you honestly what your test proved.

Its core rule: **an experiment exists to change, or confirm, a decision.** If no result would change what you do next, the skill tells you to skip the test and decide.

## What it helps you answer

1. What decision am I actually trying to make?
2. What is the most consequential thing I don't know?
3. Is a test worth running, and if so, which one?
4. What evidence would change my mind?
5. What did the experiment actually establish?
6. Given what I now know, what should I do next?

## Two modes

**Plan:** you bring an idea, request, feature, or investment. You get back an **experiment card** covering the decision at stake, the riskiest belief, one recommended test, pass, fail, and inconclusive criteria set in advance, how to run it, and what a pass would and wouldn't prove.

**Review:** you come back with results. You get a grade against the criteria you set beforehand (Pass, Fail, Inconclusive, or Invalid Test), what got stronger or weaker and on what kind of evidence, and a recommended next decision. The final call stays yours.

Still in the same chat? Just say what happened. Starting a new chat? Paste the card first, then the results.

## When to use it

### Before you commit (Plan)

| Situation | Example | What you should get |
|---|---|---|
| A customer or sales request lands | "Three enterprise customers asked for X." | The request treated as a hypothesis, not proof of demand. Usually a pricing or workflow test, not a build. |
| Leadership wants it on the roadmap | "We need an AI feature in Q1." | A gated decision ("fund it if X is true by planning lock") and one test that can answer it in time. |
| Building feels too cheap not to | A side project you could vibe-code this weekend | A test sized to your real hours. It's a build only if building answers the riskiest question. |
| It works, but will anyone pay? | A working AI feature that buyers balk at | Viability named as the open risk. A pricing test with a real number and a budget-owner question, not more feature work. |
| Pricing or packaging | Add-on vs. tier vs. included | A test aimed at money or a real commitment, with a note on what stated price acceptance can't prove. |
| A cheap, reversible change | Renaming a button | "Don't test, decide." Short reason, no card. |
| A/B test or usage metric | "How long should this onboarding test run?" | One primary metric, a minimum meaningful effect, a sample size and run length worked out in code, and other options if your traffic can't detect the effect. |

### After the test (Review)

| Situation | What you should get |
|---|---|
| You're back with results | A grade against the original criteria, with what changed and on what evidence |
| Mixed or split results | No forced verdict. The split is read as a possible segmentation signal. |
| The test was run badly | **Invalid Test**, not Fail. The belief is untested, not disproven. You also get what a valid rerun needs. |
| A pass, and you're itching to scale | No "validated" stamp. You get the next uncertainty one level up, such as retention, renewal, or procurement. |
| You want the result to say yes | Pushback: your reading next to the reading the evidence supports, with which is stronger. |

### When not to use it

- Writing a spec after the decision is made
- Diagnosing why a metric moved
- Pure execution work with no open bet

## The evidence ladder

Every test is rated by the strongest evidence it can produce. Each rung up is harder to fake.

| Rung | What it is | What it can't tell you |
|---|---|---|
| **Says** | What people tell you: interviews, surveys, "I'd use that" | Whether they'll actually use it or pay |
| **Does** | What people do: usage, workflow observation, concierge use | Whether they'll pay |
| **Pays** | Money changes hands: pre-orders, paid pilots, a signed quote | Retention and scale |
| **Commits** | A durable organizational commitment: an LOI, a PO, a renewal, a named budget owner | Long-run outcomes |

A "says" signal can justify a week of building. It can't justify a production commitment or a pricing launch.

## Examples

- [Plan example](examples/plan-example.md): an enterprise AI feature request that customers want but may not pay for
- [Review example](examples/review-example.md): the results come back, and the PM wants them to say yes

## Testing changes

[`evals/evals.json`](evals/evals.json) holds 10 test prompts with the expected behavior for each. They cover customer requests, solo builders, viability gaps, split interviews, invalid tests, pushback on a preferred conclusion, "don't test" cases, and A/B feasibility. After you edit the skill, run them with and without the skill to check that it still adds judgment, not just structure.

## Background

This skill grew out of the "build-to-learn" idea: when building gets cheaper, validation should get more frequent, not less. Its main additions to that idea are starting from the decision instead of the belief, an explicit "don't test" outcome, reviewing results as a full mode, and an evidence ladder. The "start from the decision" principle draws on Douglas Hubbard's *How to Measure Anything*: a measurement is only worth taking if it could change a decision.
