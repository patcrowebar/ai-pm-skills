# Changelog

## 1.0.0 (2026-11-03)

First public release.

- Two modes: **Plan** (experiment card) and **Review** (graded readout)
- Starts from the decision: the skill names the decision a test feeds before it designs anything
- "Don't test, decide" is a valid outcome for cheap, reversible, or decision-irrelevant questions
- Picks the riskiest belief using desirability, viability, feasibility, and usability, plus other risks where those fit better
- Recommends the lowest-effort credible test that could change the decision, not just the cheapest test
- Evidence ladder: says → does → pays → commits
- Pass bars capped at 2–3 conditions; the evidence rung must be reachable within the timebox; any change to the user's numbers must be explained
- Initiative kill criteria kept separate from experiment thresholds
- Quantitative test rules: one primary metric, minimum meaningful effect, sample size and run length worked out in code
- Four review outcomes: Pass, Fail, Inconclusive, Invalid Test
- Review always checks whether the original threshold was sound (THRESHOLD NOTE) and tags each finding with its evidence rung
- Explicit pushback when the evidence contradicts the user's preferred conclusion
- 10 eval scenarios
