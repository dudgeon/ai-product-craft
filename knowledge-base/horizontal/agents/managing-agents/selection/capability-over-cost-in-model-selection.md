---
created: 2026-02-19
updated: 2026-02-19
template: templates/knowledge-entry.md
template_version: 5
tags: [knowledge, ai-pm]
status: draft
entry_type: insight
origin: sourced
featured: false
domain: horizontal
horizontal_domain: agents
project: ai-pm
---

# Capability Over Cost in Model Selection

## Summary

Default to the most capable model available, not the cheapest. The intuition to optimize cost by using cheaper models frequently backfires: a less capable model burns more tokens correcting its own mistakes than a smarter model spends getting it right the first time. The apparent savings on per-token cost are offset by increased iteration cycles, re-runs, and the human time spent untangling errors that a better model wouldn't have made.

Boris Cherny runs Opus 4.6 at maximum effort for everything. Not as a luxury — as a productivity decision. This generalizes: the total cost of a task includes the human review time, the iteration loops, and the compounding errors when an underpowered model starts from a bad first draft. Capable models usually win on total cost even when they lose on per-token cost.

## How to Apply

- **Default to the highest-capability model for agentic tasks.** Agentic tasks compound errors across many steps; a single early mistake can cascade. Capable models are particularly valuable here.
- **Use cheaper models for genuinely simple tasks.** Classification, extraction, summarization of short text — tasks where the bar is low and the failure mode is obvious. Don't use a cheap model as the default and move up when stuck; start capable and move down when you've proven you can.
- **Measure total cost, not token cost.** Track: how many iterations does it take to get an acceptable result? How much human review time? What's the re-run rate? These factors often make the expensive model cheaper in practice.
- **Don't let cost optimization assumptions drive architecture decisions.** Building a product around a cheap model's limitations creates technical debt that's hard to unwind when you realize the savings weren't real.

Counterpoint: at scale, token cost does matter. The "use max-capable model" principle applies most strongly during experimentation and for tasks with non-trivial complexity. High-volume, well-understood tasks with simple success criteria are candidates for model downgrade after the approach is proven.

## Sources

### From: [2026-02-19 Head of Claude Code: What Happens After Coding Is Solved](../../../../sources/2026-02-19-head-of-claude-code-boris-cherny.md)
**Key quote**: "A less intelligent model often burns more tokens correcting mistakes than a smarter one spends getting it right the first time. Boris runs maximum effort on Opus 4.6 for everything."
**Attribution**: Boris Cherny
**What this source adds**: Empirical basis from someone shipping 10–30 PRs daily. Cherny's claim isn't about preference — it's about observed token economics. The smarter model is cheaper in practice because it iterates less.
**Links**: [Original](https://www.lennysnewsletter.com/p/head-of-claude-code-what-happens) | [Archive](../../../../sources/2026-02-19-head-of-claude-code-boris-cherny.md)

## Related

- [Model Fit for Qualitative Analysis Tasks](model-fit-for-qualitative-analysis.md) — Complementary: task-type determines *which* capable model (Claude vs. Gemini vs. ChatGPT); this entry determines the tier (capable vs. cheap)
- [Delay Token Cost Optimization](../../../ai-adoption/delay-token-cost-optimization.md) — Related: don't optimize token cost during experimentation; same logic applies to model tier selection
- [Plan Mode as Claude Code Default](../harnesses/plan-mode-as-claude-code-default.md) — Pairs with Opus 4.6; plan mode + capable model is Cherny's default workflow
