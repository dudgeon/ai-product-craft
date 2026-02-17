---
created: 2026-02-16
updated: 2026-02-16
template: templates/knowledge-entry.md
template_version: 4
tags: [knowledge, ai-pm, mental-model, agents, managing-agents, task-fit, delegation, decision-framework]
status: draft
entry_type: mental-model
origin: sourced
featured: false
domain: horizontal
horizontal_domain: agents
project: ai-pm
---

# Delegation Decision Framework

## Summary

A three-variable equation for deciding when to delegate work to AI agents: **Human Baseline Time × Probability of Success × AI Process Time**. Delegation is worthwhile when the task takes humans a long time, the AI's probability of producing acceptable output is high, and the cost of evaluating AI output is low relative to doing the work yourself.

The tradeoff: you're exchanging "doing the whole task" against "paying the overhead cost" of requesting, waiting, and evaluating — possibly multiple times. A 1-hour task with 30-minute evaluation overhead only works if success probability is very high. A 10-hour task justifies several hours of working with AI even at moderate success rates.

This framework becomes more favorable over time as AI capability improves (increasing Probability of Success) and as the human gets better at delegation (reducing AI Process Time through better instructions and faster evaluation).

## How to Apply

**When to use**: Before delegating any non-trivial task to an AI agent. Estimate the three variables and do the rough math. This prevents both under-delegation (doing work yourself that AI could handle) and over-delegation (wasting time on tasks where AI is unlikely to succeed).

**When not to use**: For trivial tasks (< 5 minutes) where the overhead of deciding exceeds potential savings. Also less useful for creative/exploratory tasks where "success" is hard to define upfront.

**The three variables**:

1. **Human Baseline Time** — How long does this task take you? Longer tasks make delegation increasingly attractive because even a moderate success rate saves significant time.
2. **Probability of Success** — How likely is the AI to produce acceptable output? This varies by task type and is hard to predict (the "jagged frontier" — you don't reliably know what AI will be good or bad at). When uncertain, the low cost of trying shifts the math toward delegation.
3. **AI Process Time** — The full cost of delegation: crafting the request, waiting, evaluating the output, providing feedback, iterating. Includes failed attempts. Better instructions and faster evaluation directly reduce this.

**Evidence**: OpenAI's GDPval study tested human experts vs GPT-5.2 on diverse professional tasks. Expert tasks averaged 7 hours (Human Baseline Time). AI took minutes but evaluation took ~1 hour (AI Process Time). Probability of Success reached ~72% (tied or beat experts). Result: ~3 hours saved on average per 7-hour task. Failed attempts cost more (wasted prompting + review time), but successes are much faster.

**Three levers to improve the equation**:
1. **Give better instructions** — clear goals increase Probability of Success
2. **Get better at evaluation and feedback** — fewer iteration attempts needed
3. **Make evaluation cheaper** — less time to assess quality

All three levers are improved by subject matter expertise — experts know what instructions to give, spot errors faster, and correct more efficiently. This is why [management skills matter more than AI skills](../talent-to-direction-scarcity-shift.md).

**The jagged frontier implication**: Because you can't reliably predict what AI will succeed at, and because AI is fast and cheap, the optimal strategy is often to *just try it* — generate multiple versions and throw most away. The framework's value is in avoiding clearly losing bets (low baseline time + low success probability), not in precisely predicting winners.

**For AI PMs**: This framework directly informs product decisions about agent capabilities. If your users' tasks have high Human Baseline Time and your agent's Probability of Success is increasing, the value proposition is clear. Focus investment on reducing AI Process Time (better evaluation UX, faster feedback loops) and increasing Probability of Success (better context, domain-specific tuning).

## Sources

### From: [2026-01-27 Management as AI Superpower](../../../sources/2026-01-27-ethan-mollick-management-as-ai-superpower.md)
**Key quote**: "You are making a trade-off: the time you would have spent on the whole task vs. paying the overhead cost, potentially several times."
**Attribution**: Ethan Mollick
**What this source adds**: Introduces the three-variable framework with quantitative backing from GDPval. The key contribution is framing delegation as a *math problem* rather than a gut feeling — and showing that the math increasingly favors delegation as AI capability improves. The "three levers" for improvement give actionable optimization paths.
**Links**: [Original](https://www.oneusefulthing.org/p/management-as-ai-superpower) | [Archive](../../../sources/2026-01-27-ethan-mollick-management-as-ai-superpower.md)

## Related

- [Talent-to-Direction Scarcity Shift](../talent-to-direction-scarcity-shift.md) — the thesis-level insight that makes this framework increasingly important: as talent becomes abundant, the ability to direct it well is the differentiator
- [Delegation Documentation as Agent Prompts](../delegation/delegation-documentation-as-prompts.md) — once you've decided TO delegate using this framework, the delegation craft entry covers HOW
- [Parallel Prototyping for Clarity](../../../../product-lifecycle/shape/parallel-prototyping-for-clarity.md) — operationalizes the jagged frontier implication: when success is uncertain, generate multiple versions cheaply
