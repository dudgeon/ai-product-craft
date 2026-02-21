---
created: 2026-02-19
updated: 2026-02-19
template: templates/knowledge-entry.md
template_version: 5
tags: [knowledge, ai-pm]
status: draft
entry_type: technique
origin: sourced
featured: false
domain: horizontal
horizontal_domain: agents
project: ai-pm
---

# Plan Mode as Claude Code Default

## Summary

Start 80% of Claude Code tasks in plan mode. Plan mode is a single-sentence injection: "don't write code yet." That's the whole mechanism — one sentence that tells the model to plan before acting. The agent works through the problem, produces a plan, and waits for human review before touching any files.

The payoff: once the plan looks right, Boris Cherny auto-accepts edits and Claude Code one-shots the implementation nearly every time with Opus 4.6. The brief upfront pause — reviewing a plan instead of reviewing code — produces dramatically better outcomes than diving straight into implementation. You catch misunderstandings at the cheapest possible moment.

## How to Apply

1. **Activate plan mode** before describing the task. In Claude Code, this can be done with a slash command or by prefacing your prompt with an instruction not to write code yet.
2. **Review the plan before accepting.** The plan is where you catch scope misunderstandings, missing context, or wrong approach — not after 200 lines of code have been written.
3. **Correct the plan, not the code.** If the plan is wrong, fix it in prose before the agent touches files. Prose corrections are cheaper than code corrections.
4. **Auto-accept after a good plan.** Once the plan accurately reflects what you want, let the agent run without interruption. With Opus 4.6, one-shot implementation is common from a good plan.
5. **Use it for 80% of tasks.** The remaining 20% are genuinely simple — clear enough that planning overhead doesn't pay off. Develop a feel for which tasks need it.

The underlying principle: align on the approach before generating implementation. Plan mode simply makes this structured and enforced. It's the equivalent of "no coding before design" applied to agent workflows.

## Sources

### From: [2026-02-19 Head of Claude Code: What Happens After Coding Is Solved](../../../sources/2026-02-19-head-of-claude-code-boris-cherny.md)
**Key quote**: "Boris begins 80% of his tasks there. All it does is inject one sentence telling the model not to write code yet. Once the plan looks right, he auto-accepts edits and it one-shots the implementation almost every time with Opus 4.6."
**Attribution**: Boris Cherny
**What this source adds**: First-person workflow from the creator of Claude Code. Cherny ships 10–30 pull requests daily using this technique — the volume validates the method. The "one sentence" framing demystifies what plan mode is and why it works.
**Links**: [Original](https://www.lennysnewsletter.com/p/head-of-claude-code-what-happens) | [Archive](../../../sources/2026-02-19-head-of-claude-code-boris-cherny.md)

## Related

- [Capability Over Cost in Model Selection](../managing-agents/selection/capability-over-cost-in-model-selection.md) — Plan mode pairs with Opus 4.6 for best results; the two techniques reinforce each other
- [Stepwise Task Execution](../system-design/supervision/stepwise-task-execution.md) — Plan mode is a specific implementation of the broader stepwise principle: pause before proceeding
- [Cursor: Structured AI Development](cursor-structured-ai-development.md) — Cursor's three-file system is a parallel approach to structured, plan-first AI development
