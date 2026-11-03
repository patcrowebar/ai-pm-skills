# ux-review

**Review or shape any product experience against a clear UX thesis, including AI features.**

Most UX feedback is either taste ("make it cleaner") or a checklist ("fewer clicks"). This skill applies a fixed thesis instead, built on eight principles and four AI-native expectations. It turns them into concrete findings, fixes, requirements, and tests.

## The thesis in one line

> An excellent user experience helps people accomplish meaningful goals with the least unnecessary effort, while preserving the understanding, confidence, and control needed to achieve good outcomes.

For AI-native software, the purpose of AI isn't to remove the human from every workflow. It's to make the human more capable: automate what doesn't need judgment, and strengthen judgment where it matters.

### Eight principles

1. **Valuable:** helps users achieve outcomes that matter, not just finish interactions
2. **Clear:** purpose, current state, and next step are understandable
3. **Effortless Where Possible:** removes unnecessary effort, but keeps friction that protects
4. **Predictable:** users can form an accurate mental model, even when AI output varies
5. **Responsive:** fast, with honest progress and no fake success states
6. **Forgiving and Controllable:** easy to review, undo, correct, and recover
7. **Contextual and Continuous:** surfaces what matters now and preserves context across sessions
8. **Trustworthy and Inclusive:** honest, secure, and accessible, with trust matched to how reliable the product actually is

### Four AI-native expectations

1. **Intelligence in Context:** AI works inside the real workflow, not as a chatbot by default
2. **Inspectable Intelligence:** users can see the evidence, assumptions, and limits behind an output
3. **Appropriate Autonomy:** automate low-risk work, keep humans in control of consequential decisions
4. **Correctable and Improving AI:** users can edit, reject, rerun, or reverse, right inside the workflow

## Modes

| Mode | Use it for | You get |
|---|---|---|
| **Full review** | A multi-screen flow, a prototype, a pre-launch check | A rating per principle (Strong / Adequate / Gap / N/A) with evidence, top fixes, the tensions between principles, and what still needs testing |
| **Quick review** | One screen, a gut check, limited time | A verdict, the top 3 fixes, the one thing to keep, and one cheap test, in under 200 words |
| **Spec injection** | A PRD, brief, or user story | A UX Requirements section covering states, errors, reversibility, continuity, accessibility, and AI behavior, plus Given/When/Then acceptance criteria |
| **Build-prompt hardening** | A prompt for Claude Code, Cursor, Lovable, Replit, v0, and similar tools | The full revised prompt, ready to paste, with the states, recovery, and accessibility these tools skip by default |
| **Trade-off resolver** | "Auto-apply or ask first?" and other competing goals | A documented decision using the five-factor test, plus the condition that would reverse it |
| **AI feature audit** | Any AI-powered feature, agent, or output | A check on whether AI is the right tool at all, a rating for each AI-native expectation, an autonomy table, and the "interaction contract" |
| **Measurement plan** | "How do we know this UX works?" | Signals for effectiveness, efficiency, and experience, with a note on how to interpret each AI signal |

## What makes it different

- **No single UX score.** Every principle is rated separately, with evidence.
- **Evidence is labeled.** Each finding is marked *Observed*, *Assumed*, or *Needs testing*.
- **The numbers get checked.** If a screen shows totals, timelines, or prices, the skill does the math and shows any mismatch.
- **It pushes back on UX dogma.** It doesn't assume fewer clicks, confirmation dialogs everywhere, chat-first AI, or polish are good by default.
- **Every output ends with a test:** the cheapest real-user signal that would confirm or overturn the recommendation.

## Examples

- [Quick review](examples/quick-review-example.md): a checkout screen with a pricing mismatch
- [Trade-off resolver](examples/tradeoff-example.md): should an AI inbox assistant auto-archive emails or ask first?

## Testing changes

[`evals/evals.json`](evals/evals.json) holds test prompts covering each mode, plus anti-dogma and numbers-check cases. Run them after any edit to confirm the skill still gives grounded, specific feedback.
