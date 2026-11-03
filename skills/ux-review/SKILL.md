---
name: ux-review
description: Review or shape a product workflow, screen, spec, build prompt, or AI feature against a UX thesis of eight principles and four AI-native expectations. Use for UX reviews (full or quick), adding UX requirements and acceptance criteria to a spec, hardening a prompt for a vibe-coding tool, resolving UX trade-offs like auto-apply vs. ask first, auditing the experience of an AI feature, or planning how to measure whether a UX works.
---

# UX Review

Apply **the UX Thesis** below to real product work: screens, flows, prototypes, specs, build prompts, and AI features.

## 1. Rules of use

- The thesis is the source of truth for every review. Its **eight principles** and **four AI-native expectations** are fixed within this skill.
- Never rename, merge, add to, or re-rank them, so reviews stay comparable over time. Product-specific *emphasis* is allowed. If the user wants to change the framework itself, say that's a change to the skill, not something to improvise in a review.
- **Apply, don't recite.** Turn principles into concrete workflow choices, states, error handling, verification affordances, and measurable outcomes. A response that only restates principles has failed.
- **No single UX score.** Do not produce numeric scores like "7/10". Rate each principle as **Strong / Adequate / Gap / N/A**, with evidence.
- **Separate evidence from judgment.** Label claims as *Observed* (seen in the artifact or data), *Assumed* (inferred), or *Needs testing*.
- Never call an interface excellent because it is fashionable, visually minimal, or AI-powered.

## 2. Pick the mode

Work out which job is being asked for. If it's unclear, default to **Review**. Modes can be combined (for example, Review followed by Spec injection).

| Mode | Trigger examples | Output |
|---|---|---|
| A. UX Review (Full) | "review this flow", "full review", several screens, a whole flow or prototype | Principle-by-principle review + prioritized fixes |
| A2. Quick Review | "quick review", "quick look", "gut check", "anything jump out?", a single screen, or the user signals limited time | Verdict + top 3 fixes + one test |
| B. Spec Injection | PRD, Build Brief, user story, feature brief | UX requirements + acceptance criteria to add |
| C. Build-Prompt Hardening | a prompt for Claude Code, Lovable, Replit, Cursor, v0 | The complete, revised prompt, ready to paste |
| D. Trade-off Resolver | "should this auto-apply or ask first?", competing goals | Documented decision using the 5-factor test |
| E. AI Feature Audit | any AI-powered feature, agent, or output flow | AI-native expectations + probabilistic realities audit |
| F. Measurement Plan | "how do we know this UX works?" | Effectiveness / Efficiency / Experience signals + AI indicators |

**Full vs. Quick:** use Quick for a single screen or when the user asks for speed. Use Full for multi-screen flows, pre-launch reviews, or high-stakes products. If unsure, run Quick and offer the Full review in one closing line. If a Quick review turns up a High-impact safety, data-integrity, or trust issue, say so plainly and recommend the Full review.

## 3. The framework

### Core thesis
An excellent user experience helps people accomplish meaningful goals with the least unnecessary effort, while preserving the understanding, confidence, and control needed to achieve good outcomes.

For AI-native software: The purpose of AI isn't to remove the human from every workflow. It's to make the human more capable, automating what doesn't require judgment and strengthening judgment where it matters.

Excellent UX is not synonymous with beautiful screens, fewer clicks, shorter sessions, higher engagement, or more automation. A good interface makes software easy to operate. An excellent experience helps the user succeed.

**Value vs. experience.** Product value asks: *Is this a meaningful problem worth solving?* Experience quality asks: *How effectively does the product help the user realize that value?* Evaluate UX in the context of the outcome the product exists to enable. For decision-oriented products, judge whether the user made a well-informed, defensible decision, not only whether the result was favorable.

### The eight core UX principles

1. **Valuable.** The experience helps users achieve meaningful outcomes, not merely complete interactions. Design backward from the user's objective. *Test: Did this experience help the user accomplish something that mattered?*
2. **Clear.** The product makes its purpose, current state, and next appropriate action understandable. Plain language, meaningful hierarchy, visible status, explicit consequences, without assuming every screen needs exactly one action. *Test: Can the user understand where they are, what is happening, and what they can do next?*
3. **Effortless Where Possible.** Removes unnecessary cognitive load, steps, decisions, repetition, and waiting. Preserve necessary complexity. Friction that prevents harm, supports verification, or improves consequential judgment can be valuable. *Test: Is the effort demanded by the experience necessary for the user's goal?*
4. **Predictable.** Behaves consistently, and outcomes and patterns are understandable. For probabilistic AI, consistency means consistent expectations, clear boundaries, and understandable ways to handle variation, not identical outputs. *Test: Can users form an accurate mental model of how the product behaves?*
5. **Responsive.** Responds promptly and communicates progress honestly, covering both technical speed and workflow effort. Never show an optimistic success state that misrepresents what happened. *Test: Does the user know that the product is working, and is the time spent justified?*
6. **Forgiving and Controllable.** Helps users avoid mistakes and makes review, correction, reversal, and recovery straightforward. Prefer undo over needless confirmation for reversible actions, and use previews, explicit authorization, and stronger safeguards for consequential ones. Explain errors in task terms, with a path forward. *Test: When something goes wrong, or the user changes their mind, can they regain control?*
7. **Contextual and Continuous.** Surfaces what matters now and preserves useful context over time: resumption across sessions and devices, graceful handling of interruptions, partial failures, and offline or degraded states. It adapts without surprising users, hiding meaningful options, or retaining information against their expectations. *Test: Can the user pick up where they left off without having to rebuild context or fight unwanted assumptions?*
8. **Trustworthy and Inclusive.** Earns appropriate trust through reliable, transparent, secure, accessible, honest behavior. Accessibility is a baseline, not an add-on. Trust is calibrated to actual reliability, not maximized through reassuring language or decorative confidence scores. *Test: Can people with different abilities and circumstances use the product and rely on it to the degree its evidence warrants?*

**On delight:** Delight is an amplifier, not a substitute. Polish never outranks clarity, recovery, trust, or user outcomes. In serious tools, delight often comes from competence.

### Four AI-native expectations (in addition to the eight)

1. **Intelligence in Context.** AI assists inside the real workflow, not as a disconnected chatbot by default. Use the interaction that serves the task (form, table, suggested action, comparison, conversation, background assistance). Don't use AI when a simpler deterministic mechanism is more reliable and understandable.
2. **Inspectable Intelligence.** Users can evaluate the basis, limitations, and consequences of AI outputs: evidence, provenance, assumptions, uncertainty, previews, comparisons, diffs. Distinguish observed facts from inferences and recommendations. A fluent explanation is not proof. A confidence score is not verification, and it shouldn't be presented as a probability unless it is calibrated.
3. **Appropriate Autonomy.** Automate mechanical, low-risk work, and keep meaningful human control over consequential decisions. Set autonomy by impact, reversibility, authorization, and the cost of error. Preview or seek approval before hard-to-reverse actions, and don't add needless confirmation for safe, reversible work.
4. **Correctable and Improving AI.** Users can challenge, edit, reject, rerun, or reverse outputs and actions, and correction lives inside the primary workflow. Learn from feedback only with suitable privacy and data-governance safeguards, aiming at better future performance, not the appearance of intelligence.

### Realities of probabilistic AI
- **Nondeterminism:** make meaningful differences inspectable rather than pretending outputs are stable.
- **Uncertainty:** provide verifiable evidence and ways to question, test, or correct. Persuasive wording is not reliability.
- **Latency:** set accurate expectations, show honest progress, preserve work, and support interruption or continuation.
- **Change over time:** when comparisons or release decisions matter, make model, prompt, data, and eval versions visible.
- **Central distinction:** output need not be deterministic, but the *interaction contract* (what the product will do, how uncertainty is handled, what control the user keeps) must stay understandable and dependable.

## 4. Trade-offs: make them explicit

Excellent UX does not maximize every principle at once. There is no fixed ranking.

| Tension | How to decide |
|---|---|
| Simplicity vs. power | Approachable for newcomers without constraining experts. Use hierarchy and progressive disclosure, not blanket removal. |
| Speed vs. confidence | Remove pointless waiting, and keep time for review when mistakes are consequential. |
| Personalization vs. predictability | Use context to cut repetition, and keep adaptations legible, adjustable, unsurprising. |
| Automation vs. control | Automate reversible, low-risk tasks. Require visibility or authorization for high-impact actions. |
| Transparency vs. cognitive load | Decision-relevant evidence first, with a path to deeper inspection. Never bury material uncertainty. |
| Consistency vs. flexibility | Reuse familiar patterns unless a distinct workflow demonstrably needs something else. |

**Five-factor test** (use for every meaningful trade-off):
1. **User goal:** what is the person actually trying to accomplish?
2. **Consequences:** what happens if they misunderstand, accept a wrong result, or err?
3. **Reversibility:** how easily can it be corrected or undone?
4. **User and context:** expertise, environment, urgency, accessibility needs.
5. **Evidence:** what research, observed behavior, or testing supports the choice?

High cost of error means verification, clarity, and control usually beat raw speed. Low-risk and easily reversible actions mean efficiency may reasonably win. Document the trade-off, and never invoke a principle as a slogan.

## 5. Mode playbooks

Before any mode, establish briefly: **who the user is, what outcome they're after, and what is at stake if it goes wrong.** If the material doesn't say, state your assumption and mark it *Assumed*. Don't stall on questions unless the stakes or the scope truly hinge on the answer.

### Data-consistency check (runs in A, A2, and E whenever the artifact shows numbers)
The user will never add the numbers up, but if they don't reconcile, trust is quietly wrong. Before rating anything, do the arithmetic yourself:
- **Totals vs. parts:** do the line items sum to the totals shown (counts, durations, prices, percentages)?
- **Timelines:** do start time + durations = the end times shown? Do sequential steps chain without gaps or overlaps?
- **Same value, different places:** does a number or label that appears in two places agree, and does one label ever mean two different things?
- **Units and rounding:** consistent units, and does rounding drift accumulate into a visible mismatch?
- **Implied buffers or hidden terms:** if a gap is explained by something the UI never states (a buffer, a fee, a minimum), flag that as a Clear / Trustworthy issue.

Show the actual math in the finding ("41 + 108 = 149 min, but 5:00 to 7:44 is 164 min"). Mark each mismatch *Observed*, and when there is a plausible explanation, state it as *Assumed*. Rate impact by consequence: a mismatch in a safety, money, or deadline number is **High**. If no numbers are shown, skip this check silently.

### A. UX Review (Full)
Inputs: screenshots, flow, prototype, URL, or description. If you can see the artifact, cite specifics ("the Save button gives no saved state").

Run the data-consistency check first, then run the **Practical UX Review**:
1. **Outcome:** what meaningful goal, and how will we know they succeeded?
2. **Clarity:** can they tell what's happening, what matters, and what to do next?
3. **Effort:** which steps, inputs, waits, or decisions are unnecessary, and which are intentionally protective?
4. **Expectations:** are behavior, state, and consequences predictable, even if AI outputs vary?
5. **Control:** can they inspect, correct, reject, undo, or recover at the level the risk warrants?
6. **Continuity:** is context preserved across interruptions and returns?
7. **Trust and access:** honest about limits, accessible, private, appropriately secure?
8. **AI, if present:** right mechanism? Can users verify what matters? Is autonomy proportional?
9. **Trade-offs:** which principles compete, what was prioritized, and why?
10. **Evidence:** what real behavior or results would confirm it works?

Output template:
```
## UX Review: <workflow>
User · Outcome · Stakes (one line each)

### Verdict
2–3 sentences: does this help the user finish the right work, at suitable quality, with no more effort than needed?

### Principle ratings
| Principle | Rating | Evidence (Observed/Assumed) |
(8 rows; add 4 AI-native rows if AI is present; N/A allowed)

### Numbers check
Mismatches found, with the math shown, or "All shown numbers reconcile." (omit if no numbers)

### Top fixes (max 5, highest impact first)
1. <Problem> → <Specific change> · Principle(s) · Impact: High/Med/Low

### Tensions
Each: the competing principles, the call, the 5-factor reasoning in one or two lines.

### What we still don't know
Needs-testing items + the cheapest test for each.
```

### A2. Quick Review
Same rigor, less output. Run the data-consistency check and scan all ten Practical UX Review questions internally, but report only what matters most. No principle ratings table.

Output template:
```
## Quick UX Review: <screen or flow>
User · Outcome · Stakes (one line)

**Verdict:** 1–2 sentences.

**Top 3 fixes**
1. <Problem> → <Specific change> · Principle · Impact
2. …
3. …

**Keep:** the one thing working best (so it survives the fixes).

**Test it:** the single cheapest real-user check.
```
Keep it under ~200 words. Include a number mismatch as a fix only if it ranks in the top 3. End with one line offering the Full review if the flow warrants it.

### B. Spec Injection
Read the spec, then add a **UX Requirements** section rather than rewriting the spec:
- **States:** empty, loading/processing, saved, proposed, awaiting decision, complete, partial failure, failed, offline/degraded, with what the user sees in each.
- **Errors and recovery:** each likely failure, its task-language message, and the path forward.
- **Reversibility map:** which actions are reversible (undo, no confirm) and which are consequential (preview/authorize).
- **Continuity:** what persists across sessions/devices, and what happens on interruption.
- **Accessibility baseline:** keyboard paths, labels, contrast, no color-only meaning, screen sizes.
- **Data consistency:** any displayed totals, timelines, or derived numbers must reconcile with their parts, and any buffer or hidden term must be shown.
- **AI (if present):** verification affordances, autonomy level per action, correction path, version visibility.
- **UX acceptance criteria:** Given/When/Then, testable, at least one per principle that materially applies.
- **Success signals:** pull from Mode F.

### C. Build-Prompt Hardening
Vibe-coding tools skip states, recovery, and accessibility by default. Return the **complete revised prompt in one copy-paste block**, never fragments or diffs to stitch together. Add explicit instructions for: all UI states above, honest progress (no fake success), undo for reversible actions, confirmation only for destructive ones, task-language errors, keyboard and screen-reader basics, preserving user input on failure, displayed numbers that reconcile with their parts (with buffers labeled), and for AI features, showing sources or diffs and an edit/reject/rerun path. Keep the user's original intent and voice. Below the block, list in 3–6 bullets what was added and why (principle names).

### D. Trade-off Resolver
```
## Decision: <question>
Tension: <Principle A> vs. <Principle B>
1. User goal: …
2. Consequences: …
3. Reversibility: …
4. User & context: …
5. Evidence: … (or "none yet": flag it)
Call: <decision>, and the condition under which we'd reverse it.
How we'll know: <observable signal>
```

### E. AI Feature Audit
1. **Is AI the right mechanism?** Name the deterministic alternative and why it does or doesn't win.
2. Rate the four AI-native expectations (Strong/Adequate/Gap/N/A, with evidence).
3. Check each probabilistic reality: nondeterminism, uncertainty, latency, change over time.
4. Run the data-consistency check on any AI-produced numbers, summaries, or counts shown to the user.
5. **Autonomy table:** each AI action → impact, reversibility, current autonomy, recommended autonomy.
6. **Interaction contract:** write in 3–5 plain sentences what the product promises the user about what AI does, how uncertainty is shown, and what control they keep. If it can't be written cleanly, that's the top finding.
7. Fixes, then Mode F signals.

For model quality, safety, cost, and latency, use a separate model-evaluation process. This mode covers the *experience* of AI, not model performance.

### F. Measurement Plan
No single KPI proves UX quality. Cover all three dimensions:

| Dimension | Question | Pick signals like |
|---|---|---|
| Effectiveness | Did users achieve the intended outcome, at required quality? | Task success, output accuracy/usefulness, decision quality, downstream outcomes, avoidable errors |
| Efficiency | What necessary and unnecessary effort did success take? | Time to first meaningful value, time to appropriately verified outcome, repeated steps, rework, context switches |
| Experience | Did users feel informed, capable, appropriately in control? | Observed hesitation, comprehension, recovery success, accessibility issues, satisfaction, calibrated confidence |

For AI: verification behavior, acceptance, edit, override, rerun rates, and recovery success. These are **diagnostic, not targets**. High acceptance can mean quality *or* uncritical reliance, and high override can mean bad output *or* healthy judgment. Always say how each signal will be interpreted against output quality, task risk, and outcomes.

When the product makes predictions (times, counts, costs), include **prediction accuracy** as an effectiveness signal: predicted vs. actual, and the threshold that would trigger recalibration.

Never optimize blindly for shorter time-on-task, fewer decisions, longer sessions, higher engagement, or higher confidence.

## 6. Reference products (illustrations, not templates)

Use these to make a principle concrete, as in "the way Cursor shows a diff before applying". Never use them as "make it look like X". Describe the pattern, not current product specifics, because products change.

| Product | Pattern it illustrates | Principles |
|---|---|---|
| Linear | Sophisticated software that stays focused and fast without sacrificing power; keyboard-first expert paths alongside clear defaults | Clear, Responsive, Predictable, Effortless Where Possible |
| Todoist | Useful work in moments without first learning a system; low cognitive load | Valuable (early), Effortless Where Possible, Clear |
| 1Password | Excellent UX doesn't mean removing safeguards; friction placed where it protects | Trustworthy and Inclusive, Effortless Where Possible (protective friction), Forgiving and Controllable |
| Figma | Complex professional work without artificial simplification; collaboration, history, continuity | Contextual and Continuous, Forgiving and Controllable, Simplicity-vs-power trade-off done well |
| Cursor | AI does meaningful work while human review stays in the loop; changes shown as reviewable diffs | Appropriate Autonomy, Inspectable Intelligence, Correctable and Improving AI |
| Perplexity | AI answers become more useful when users can examine the supporting evidence | Inspectable Intelligence, Trustworthy and Inclusive |
| Duolingo | Consumer onboarding that delivers value before asking for commitment; delight as amplifier | Valuable (early), Effortless Where Possible, note on delight |
| Stripe Dashboard | High-stakes operations (money, refunds, keys) with clear state, previews, and graduated safeguards | Clear, Forgiving and Controllable, Trustworthy and Inclusive, Automation-vs-control |

When a review would benefit from a counter-pattern, describe the anti-pattern generically and don't name a product.

## 7. Anti-dogma guardrails

Do **not** assume any of these are good by default:
- One action per screen
- Fewer clicks at all costs
- Confirmation everywhere
- Chat-first AI
- Constant personalization
- Automatic acceptance of AI output
- Polish, animation, or clever copy as evidence of quality

The same philosophy applies differently when expertise, task complexity, accessibility needs, reversibility, and risk differ. Name which of those drove a recommendation.

## 8. Output standards (every mode)

- Lead with the verdict or the decision, not with a framework recap.
- Tie every finding to a named principle or expectation, using the exact names from the framework.
- Name at least one tension when recommendations compete, along with the call (Full review and Trade-off modes. Optional in Quick).
- Mark Observed / Assumed / Needs testing.
- When numbers are shown, show your arithmetic for any mismatch rather than asserting it.
- End with **how to test it**: the cheapest real-user signal that would confirm or overturn the recommendation.
- The bar: a design is not excellent merely because users finish the flow. It should help them finish the right work, at suitable quality, with no more effort than the situation requires.

**Final standard:** Make the mechanics of software easier, the work more effective, and consequential outcomes more understandable, verifiable, and correctable.