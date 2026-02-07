---
created: 2026-02-07
updated: 2026-02-07
template: templates/knowledge-entry.md
template_version: 1
tags: [knowledge, ai-pm-craft, technique, cursor, structured-development]
status: draft
entry_type: technique
domain: professional-development
project: ai-pm-craft
---

# PRD-Driven AI Development

## Summary

A three-file rule system that structures AI-assisted development from a high-level feature idea through a complete PRD to an executable task list, with human-in-the-loop checkpoints at each stage. Instead of telling an AI to "build a feature," you guide it through progressive decomposition: first generate requirements, then break into tasks, then execute one task at a time with explicit approval between steps.

The key insight is that this isn't just project management — it's a way to force the right amount of context into the AI at each stage, preventing the compounding errors that happen when you skip straight to code.

## How to Apply

**When to use**: Any feature or project complex enough that "just build it" would fail — roughly anything taking more than a single session.

**When not to use**: Trivial changes (button color, copy tweaks) where the overhead of PRD generation isn't justified.

**Steps**:
1. Create a `generate_prd.md` rule file that tells the AI how to ask clarifying questions and produce a PRD. Key instruction: write it "suitable for a junior developer to understand" — this forces the right level of explicitness.
2. Create a `generate_tasks.md` rule file that decomposes a PRD into nested tasks with Markdown checkboxes. AI proposes a high-level plan first and waits for approval before detailing sub-tasks.
3. Create a `task_list_management.md` rule file that has the AI work through tasks one at a time, checking off each box and pausing for human approval before moving on.
4. Execute sequentially: @-include the relevant rule file in each Cursor chat. The one-step-at-a-time execution catches errors before they compound.

**For AI PMs**: This technique is directly applicable to working with engineering teams using AI. The PRD format doubles as both AI instruction and human communication artifact. The task decomposition step replaces manual ticket creation.

## Sources

### From: [[2026-02-07-ryan-carson-structured-ai-development]]
**Key quote**: "The biggest mistake that I do, that everyone does is they try to rush through the context where you just don't have the patience to tell the AI what it actually needs to know to solve your problem. And I think if we all just slow down a tiny bit and do these two steps, it speeds everything up."
**What this source adds**: The complete three-file implementation with open-source rule files. Carson's approach is notable for its simplicity — three markdown files that compose into a full development workflow. The "junior developer" framing is the key detail that makes PRDs AI-friendly.
**Links**: [Original](https://www.chatprd.ai/how-i-ai/ryan-carsons-3-step-playbook-for-structured-ai-development-in-cursor) | [[2026-02-07-ryan-carson-structured-ai-development|Archive]]

## Related

- [[context-first-development]]
- [[deliberate-context-selection]]
