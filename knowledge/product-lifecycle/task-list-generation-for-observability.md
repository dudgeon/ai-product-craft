---
created: 2026-02-07
updated: 2026-02-07
template: templates/knowledge-entry.md
template_version: 2
tags: [knowledge, ai-pm-craft, technique, observability, stakeholder-engagement]
status: draft
entry_type: technique
origin: sourced
featured: false
domain: professional-development
project: ai-pm-craft
---

# Task List Generation for Observability

## Summary

A technique for decomposing a PRD into a detailed, nested task list that serves three purposes beyond simple project planning: (1) **observability** — you can see exactly what the AI agent plans to do before it does it, (2) **control** — you approve the plan before execution, creating a human-in-the-loop gate between planning and action, and (3) **stakeholder engagement surface** — the task list is a readable artifact that technical partners, reviewers, or collaborators can inspect, critique, and contribute to without needing to understand the implementation.

The mechanism: a rule file instructs the AI to first propose a high-level plan and wait for approval, then generate a full task list with nested parent tasks, sub-tasks, and sub-sub-tasks as Markdown checkboxes. This makes the AI's intended approach legible and editable before any code is written.

## How to Apply

**When to use**: When you need visibility into *how* an AI agent will approach a complex task, or when you need to give others (collaborators, reviewers, PMs) a way to engage with the plan. Especially valuable when the AI is about to do multi-step work where early mistakes compound.

**When not to use**: Single-step or clearly-defined tasks where the execution path is obvious.

**Steps**:
1. Create a `generate_tasks.md` rule file that defines how to decompose a PRD into a nested task list
2. @-include both the rule file and the PRD in a new chat
3. The AI proposes a **high-level plan first** and asks for approval — this is the human-in-the-loop gate
4. Once approved, the AI generates `TASKS.md` with nested checkboxes: parent tasks → sub-tasks → sub-sub-tasks
5. Review the task list for correctness, ordering, and completeness before starting execution

**Why this matters beyond planning**: The task list is a *communication artifact*. A technical partner can read it and say "you're missing a migration step" or "swap the order of steps 3 and 4" without needing to pair-program. This increases the surface area for collaboration — people can contribute to AI-assisted work without being the one driving the agent.

**For AI PMs**: This technique maps directly to how AI agent products should expose their planning. When an AI agent is about to take multi-step action on behalf of a user, showing the plan first (and waiting for approval) is a UX pattern worth studying. The Markdown checkbox format is also notable — it's a lowest-common-denominator format that's readable by humans, parseable by AI, and diffable in version control.

## Sources

### From: [[2026-02-07-ryan-carson-structured-ai-development]]
**Key quote**: (on the AI proposing a high-level plan first and asking for approval) "This human-in-the-loop step makes sure the plan is headed in the right direction."
**Attribution**: Ryan Carson
**What this source adds**: Carson's `generate_tasks.md` rule file is the concrete implementation. The key design choice is the two-phase generation: high-level plan → approval → detailed tasks. This prevents the AI from going deep on a wrong approach. The Markdown checkbox format is simple but powerful — it creates a living document that tracks progress as the AI works.
**Links**: [Original](https://www.chatprd.ai/how-i-ai/ryan-carsons-3-step-playbook-for-structured-ai-development-in-cursor) | [[2026-02-07-ryan-carson-structured-ai-development|Archive]]

## Related

- [[interactive-prd-writing]]
- [[stepwise-task-execution]]
- [[context-first-development]]
