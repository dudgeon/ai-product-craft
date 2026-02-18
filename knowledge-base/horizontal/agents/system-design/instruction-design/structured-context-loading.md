---
created: 2026-02-14
updated: 2026-02-14
template: templates/knowledge-entry.md
template_version: 5
tags: [knowledge, ai-pm, technique, agents, context-loading, prd, vibe-coding]
status: draft
entry_type: technique
origin: sourced
featured: false
domain: horizontal
horizontal_domain: agents
project: ai-pm
---

# Structured Context Loading

## Summary

Before each AI interaction, load a set of purpose-built files that constrain and align the agent's behavior. Instead of explaining everything in the prompt, maintain standing documents — master plan, implementation plan, design guidelines, user journeys — that the agent reads before acting. A tasks.md file breaks the plan into executable steps, giving the agent a clear scope for each session.

This pattern appears across the entire AI tooling stack at different levels of sophistication. In non-agentic tools (Lovable, ChatGPT), it manifests as manually structured PRD files the user pastes or attaches. In semi-agentic tools (Cursor), it's rule files and @ mentions. In fully agentic tools (Claude Code), it's CLAUDE.md, skills files, and directory-level instructions that auto-load. The underlying principle is the same: the agent's output quality is bounded by the structured context it receives, not by its raw capability.

The key distinction from "just write a good prompt": structured context loading separates *what persists across sessions* (plans, guidelines, rules) from *what's session-specific* (the current task). The persistent files compound — once written, they align every subsequent interaction without re-explanation. The session prompt can stay focused on the immediate task because the background context is already loaded.

## How to Apply

**When to use**: Any multi-session AI project where context must persist across interactions. Especially valuable when working with tools that don't have built-in memory or when onboarding an agent to a project's conventions.

**When not to use**: Single-shot interactions where the full context fits in one prompt. Adding file structure to a quick question adds overhead without benefit.

**Lazar Jovanovic's four-file system** (for Lovable/non-agentic tools):
1. **Master plan** — what you're building and why (the "what" document)
2. **Implementation plan** — sequence of work, dependencies, phases (the "how" document)
3. **Design guidelines** — visual parameters, component libraries, spacing rules (the "look" document)
4. **User journeys** — how people navigate through the product (the "flow" document)

These feed into a **tasks.md** that decomposes the plan into executable steps the agent can tackle one at a time.

**Equivalent patterns in agentic tools**:
- Claude Code: `CLAUDE.md` (project context) + skills files (workflow procedures) + `tasks.md` (current work)
- Cursor: `.cursorrules` + PRD files + @ mentions
- Devin: Knowledge items + session context

**Design principles**:
1. **Separate persistent from ephemeral** — plans and guidelines persist; task instructions are per-session
2. **Load before prompting** — the agent should read context files *before* receiving the task
3. **Update as you learn** — when the agent surprises you (good or bad), update the persistent files so future sessions benefit
4. **Keep files focused** — one file per concern; don't dump everything into a single mega-document

**For AI PMs**: This is the manual version of what RAG systems do automatically — curating a context window from structured sources. Understanding this pattern builds intuition for designing AI features that need persistent context. The four-file structure also maps cleanly to product artifacts PMs already create.

## Sources

### From: [2026-02-08 Getting Paid to Vibe Code](../../../../sources/2026-02-08-vibe-coding-new-ai-job.md)
**Key quote**: "Create four PRD files before serious building begins... The agent reads these files before each prompt — a structured context loading system for non-agentic AI tools."
**Attribution**: Lazar Jovanovic (via Lenny Rachitsky)
**What this source adds**: The concrete four-file PRD system as a structured context loading pattern for non-agentic tools. Jovanovic's approach demonstrates that even without built-in agent memory, you can create persistent alignment through file-based context. The tasks.md decomposition bridges the gap between high-level plans and executable agent instructions.
**Links**: [Original](https://www.lennysnewsletter.com/p/getting-paid-to-vibe-code) | [Archive](../../../../sources/2026-02-08-vibe-coding-new-ai-job.md)

## Related

- [Interactive PRD Writing](../../../../product-lifecycle/build/interactive-prd-writing.md) — Writing PRDs *with* AI; this entry is about using PRDs *to align* AI. Complementary workflows
- [Context First Development](../../../../product-lifecycle/build/context-first-development.md) — The principle that context precedes building; structured context loading is the systematic implementation of that principle
- [Deliberate Context Selection](../../../context/deliberate-context-selection.md) — Choosing which files to include; structured context loading creates purpose-built files designed to be included
- [Filesystem as Agent State](../architecture/filesystem-as-agent-state.md) — The files that persist context are a form of agent state maintained on the filesystem
- [Three-Layer Context Disclosure](../../../context/three-layer-context-disclosure.md) — The four-file system is a form of layered disclosure: master plan (index) → implementation plan (summary) → design/journeys (detail)
