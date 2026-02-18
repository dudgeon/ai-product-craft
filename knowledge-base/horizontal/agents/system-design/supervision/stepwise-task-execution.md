---
created: 2026-02-07
updated: 2026-02-08
template: templates/knowledge-entry.md
template_version: 3
tags: [knowledge, ai-pm, technique, execution, human-in-the-loop]
status: draft
entry_type: technique
origin: sourced
featured: false
domain: horizontal
horizontal_domain: agents
project: ai-pm
---

# Stepwise Task Execution

## Summary

A technique for having an AI agent execute a task list one item at a time, with an explicit pause-and-approve checkpoint after each step. The AI completes a sub-task, marks it done (checking off the Markdown checkbox), then *stops and waits* for the human to type "yes" before proceeding to the next item. This one-at-a-time cadence catches errors, linter issues, or wrong approaches before they compound across subsequent tasks.

The key insight: in AI-assisted development, errors are cheap to fix at step N but expensive to fix at step N+10 (because later steps build on earlier ones). Stepwise execution with checkpoints is an error-containment strategy — it trades speed for correctness at exactly the points where the tradeoff is worth it.

## How to Apply

**When to use**: Multi-step AI execution where later steps depend on earlier ones. Especially important for code generation, database migrations, or any sequence where a mistake in step 3 silently corrupts steps 4-10.

**When not to use**: Independent, parallelizable tasks where each item can be evaluated in isolation. In those cases, parallel execution (e.g., running multiple agents simultaneously) is better.

**Steps**:
1. Create a `task_list_management.md` rule file that instructs the AI to: read the task list, start with the first unchecked sub-task, complete it, mark `[x]` in the file, then **stop and wait**
2. @-include the rule file and the TASKS.md file
3. The AI starts with the first sub-task, makes the required changes
4. After completion, AI edits TASKS.md to check off the box and pauses
5. You review the output (check the code, run tests, inspect the change), then type "yes" or "y" to continue
6. If something is wrong, you provide corrections before the AI proceeds

**The compounding error problem**: When AI agents execute multi-step plans without checkpoints, a small mistake in an early step (wrong schema, bad assumption, misunderstood requirement) cascades through everything built on top of it. By step 10, you're debugging a tangled mess rather than fixing one wrong assumption. Stepwise execution prevents this by catching issues at the source.

**For AI PMs**: This is a concrete implementation of the "human-in-the-loop" pattern that AI products often need. The lesson: the checkpoint doesn't need to be sophisticated — a simple "yes to continue" gate is enough. The UX question for AI products is: where do you place the checkpoints? Too many and the user is babysitting; too few and errors compound. Carson's approach (one per sub-task, not per sub-sub-task) is a practical middle ground.

## Sources

### From: [2026-02-07 Ryan Carson Structured AI Development](../../../../sources/2026-02-07-ryan-carson-structured-ai-development.md)
**Key quote**: "This back-and-forth, one-step-at-a-time process is what makes the whole system so reliable. It lets Ryan catch small errors, linter issues, or other mistakes before they become bigger problems."
**Attribution**: Ryan Carson
**What this source adds**: Carson's `task_list_management.md` rule file implements this as a concrete Cursor workflow. The mechanism is simple: the AI edits the TASKS.md file to check off boxes, creating a visible audit trail. The "yes to continue" UX is minimal but effective — it keeps the human in control without requiring deep engagement at every step.
**Links**: [Original](https://www.chatprd.ai/how-i-ai/ryan-carsons-3-step-playbook-for-structured-ai-development-in-cursor) | [Archive](../../../../sources/2026-02-07-ryan-carson-structured-ai-development.md)

## Related

- [Interactive PRD Writing](../../../../product-lifecycle/build/interactive-prd-writing.md)
- [Task List Generation for Observability](../../../../product-lifecycle/build/task-list-generation-for-observability.md)
- [Context First Development](../../../../product-lifecycle/build/context-first-development.md)
