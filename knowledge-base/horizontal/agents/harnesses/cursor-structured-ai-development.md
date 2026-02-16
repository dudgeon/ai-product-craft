---
created: 2026-02-16
updated: 2026-02-16
template: templates/knowledge-entry.md
template_version: 5
tags: [knowledge, ai-pm, technique, agents, cursor, rule-files, structured-development]
status: draft
entry_type: technique
origin: sourced
featured: false
domain: horizontal
horizontal_domain: agents
project: ai-pm
---

# Cursor: Structured AI Development with Rule Files

## Summary

A concrete implementation of structured agent development inside Cursor, using rule files, @-includes, and MCP servers. Ryan Carson's three-file system turns Cursor from a "vibe coding" tool into a disciplined agent harness — the agent follows explicit workflows rather than freestyling.

The Cursor-specific mechanics that make this work: rule files (`.md` files in a `rules/` folder) encode repeatable workflows that get loaded via @-include; MCP server configuration in Cursor settings connects external tools (Browserbase, databases) without leaving the IDE; and Repo Prompt provides surgical context selection when Cursor's automatic context isn't precise enough.

## How to Apply

**Cursor-specific setup:**

### 1. Rule Files

Create a `rules/` folder at the project root with `.md` files that instruct the agent how to behave for specific workflows. Invoke by @-including: `@rules/generate_prd.md`.

Carson's three-file system ([open-sourced on GitHub](https://github.com/snarktank/ai-dev-tasks)):
- **`generate_prd.md`** — instructs agent to ask clarifying questions, then write a PRD "suitable for a junior developer." The @-include replaces copy-pasting instructions every time.
- **`generate_tasks.md`** — @-include with the PRD. Agent proposes high-level plan → waits for approval → generates `TASKS.md` with nested checkboxes.
- **`task_list_management.md`** — @-include with TASKS.md. Agent reads task list, completes first unchecked sub-task, checks it off `[x]`, then stops and waits for "yes" before proceeding.

### 2. @ Mentions for Context Control

Cursor's @-mention system is the primary mechanism for deliberate context selection:
- `@file` — include specific files
- `@folder` — include directory contents
- `@rules/...` — load rule files as behavioral instructions
- `@docs` — include documentation

For complex architectural work where automatic context introduces noise, combine @ mentions with [Repo Prompt](https://repoprompt.com/) — a desktop app that lets you visually select files, add persona instructions (e.g., "Architect"), and generate XML-tagged prompts to paste into Cursor.

### 3. MCP Server Configuration

Configure MCP servers in Cursor Settings → MCP Servers. Each server connection expands what the agent can do without leaving the IDE.

Example from Carson: Browserbase MCP for browser automation — natural language commands like "navigate to [URL] and take a screenshot" control a headless browser in the cloud. Use cases: automated front-end testing, database queries, app interaction without context-switching.

**What's Cursor-specific vs. tool-agnostic:**

| Cursor mechanic | Tool-agnostic pattern it implements |
|---|---|
| Rule files in `rules/` | [Structured Context Loading](../skills/structured-context-loading.md) |
| @-include for files | [Deliberate Context Selection](../../context/deliberate-context-selection.md) |
| Step-by-step task execution with "yes" gate | [Stepwise Task Execution](../skills/stepwise-task-execution.md) |
| MCP server settings | [Agent as Cross-Tool Workflow Hub](../skills/agent-as-cross-tool-workflow-hub.md) |
| Repo Prompt → paste into Cursor | [Deliberate Context Selection](../../context/deliberate-context-selection.md) (external tooling) |

**For AI PMs**: Cursor's rule file system is a lightweight version of what Claude Code does with CLAUDE.md and skills files. Understanding both implementations builds intuition for how agent configuration works across harnesses — same patterns, different mechanics.

## Sources

### From: [2026-02-07 Ryan Carson Structured AI Development](../../../sources/2026-02-07-ryan-carson-structured-ai-development.md)
**Key quote**: "The biggest mistake that I do, that everyone does is they try to rush through the context where you just don't have the patience to tell the AI what it actually needs to know to solve your problem."
**Attribution**: Ryan Carson
**What this source adds**: The complete three-file workflow implemented in Cursor, with open-source rule files. Carson's system demonstrates how rule files turn Cursor from a general-purpose coding agent into a structured workflow harness. The three workflows map to increasing levels of context control: rule files for process structure, MCPs for tool integration, Repo Prompt for surgical file selection.
**Links**: [Original](https://www.chatprd.ai/how-i-ai/ryan-carsons-3-step-playbook-for-structured-ai-development-in-cursor) | [Archive](../../../sources/2026-02-07-ryan-carson-structured-ai-development.md)

## Related

- [Structured Context Loading](../skills/structured-context-loading.md) — the tool-agnostic pattern; this entry is the Cursor-specific implementation
- [Stepwise Task Execution](../skills/stepwise-task-execution.md) — the tool-agnostic pattern; Carson's `task_list_management.md` is the Cursor implementation
- [Context First Development](../../../product-lifecycle/build/context-first-development.md) — the principle that motivates the three-file system
- [Interactive PRD Writing](../../../product-lifecycle/build/interactive-prd-writing.md) — the `generate_prd.md` rule file is a Cursor implementation of this technique
