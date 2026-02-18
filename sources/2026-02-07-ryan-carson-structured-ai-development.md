---
title: "Ryan Carson's 3-Step Playbook for Structured AI Development in Cursor"
created: 2026-02-07
updated: 2026-02-07
template: templates/source.md
template_version: 3
tags: [source, ai-pm, cursor, structured-development]
status: processed
source_type: article
source_url: "https://www.chatprd.ai/how-i-ai/ryan-carsons-3-step-playbook-for-structured-ai-development-in-cursor"
archive_url: "domains/professional-development/ai-pm/sources/2026-02-07-ryan-carson-structured-ai-development.md"
author: "Ryan Carson"
host: "Claire Vo"
published: 2025-05-26
discovered: 2026-02-07
summary: "Three-file rule system for structured AI dev: generate PRD (templatized, AI asks clarifying questions) → generate task list (nested checkboxes for observability) → execute one-by-one with human approval. Core thesis: 'vibe coding' fails at scale because devs rush past context. Secondary insight: use Repo Prompt for deliberate context selection ('glass box') over automatic context ('black box')."
domain: professional-development
project: ai-pm
---

# Ryan Carson's 3-Step Playbook for Structured AI Development in Cursor

**By**: Ryan Carson
**Host**: Claire Vo (ChatPRD)
**Source**: [ChatPRD - How I AI](https://www.chatprd.ai/how-i-ai/ryan-carsons-3-step-playbook-for-structured-ai-development-in-cursor)
**Type**: article (podcast summary)

## Summary

Ryan Carson's core argument is that "vibe coding" fails at scale because developers rush past context. His three-file rule system (generate PRD → generate tasks → execute one-by-one) forces structured context-building before any code is written. The secondary insight is about deliberate context control — using tools like Repo Prompt to hand-select exactly what the LLM sees rather than relying on automatic context, especially for complex architectural work.

## Key Ideas Extracted

- **[Interactive PRD Writing](../knowledge-base/product-lifecycle/build/interactive-prd-writing.md)**: Templatized rule file that instructs AI to ask clarifying questions before generating a PRD, forcing thorough context-building; "junior developer" standard ensures AI-friendly explicitness
- **[Task List Generation for Observability](../knowledge-base/product-lifecycle/build/task-list-generation-for-observability.md)**: Decomposing a PRD into a nested task list as a mechanism for observability (see the plan before execution), control (approve before action), and stakeholder engagement (readable artifact for collaborators)
- **[Stepwise Task Execution](../knowledge-base/horizontal/agents/system-design/supervision/stepwise-task-execution.md)**: One-task-at-a-time execution with pause-and-approve checkpoints after each step; catches errors before they compound across dependent tasks
- **[Context First Development](../knowledge-base/product-lifecycle/build/context-first-development.md)**: "Slow down to speed up" — the biggest mistake in AI-assisted development is rushing past context; writing PRDs "for a junior developer" forces the clarity AI needs
- **[Deliberate Context Selection](../knowledge-base/horizontal/context/deliberate-context-selection.md)**: Hand-picking files for LLM context ("glass box") vs. relying on automatic context ("black box") — for complex tasks, precise context produces dramatically better results
- **[Cursor: Structured AI Development](../knowledge-base/horizontal/agents/harnesses/cursor-structured-ai-development.md)**: Cursor-specific implementation — rule files via @-include, MCP server config, Repo Prompt integration

## Notes

The three workflows map to increasing levels of context control: rule files for process structure, MCPs for tool integration, Repo Prompt for surgical file selection. The common thread is always context quality.

The "suitable for a junior developer" instruction is clever — it forces the PRD to be explicit enough for an LLM to follow unambiguously. What's good for a junior dev is good for AI.

The MCP workflow (Browserbase, Postgres) is interesting but more of a tool demo than a reusable technique. The real insight is that MCPs collapse context-switching by bringing external tools into the IDE.

## Raw Content

Five-time founder Ryan Carson reveals his structured playbook for turning "vibe coding" into a scalable process. His philosophy: if you slow down and give the AI proper context, you actually speed everything up in the long run.

> "The biggest mistake that I do, that everyone does is they try to rush through the context where you just don't have the patience to tell the AI what it actually needs to know to solve your problem. And I think if we all just slow down a tiny bit and do these two steps, it speeds everything up."

### Workflow 1: From PRD to Executable Tasks in Cursor

A structured, repeatable process using three rule files. Open-source: [GitHub](https://github.com/snarktank/ai-dev-tasks).

**Step 1: Generating a PRD**
- Custom rule file `generate_prd.md` in a `rules` folder
- Key instruction: write PRD "suitable for a junior developer to understand"
- Invoke by @-including the rule file in Cursor chat
- AI asks clarifying questions, then generates complete `PRD.md`

**Step 2: Creating a Detailed Task List**
- Another rule file `generate_tasks.md`
- @-include both the rule and the PRD
- AI proposes high-level plan first, asks for approval (human-in-the-loop)
- Generates `TASKS.md` with nested parent tasks, sub-tasks, sub-sub-tasks with Markdown checkboxes

**Step 3: Executing Tasks Systematically**
- Third rule file `task_list_management.md`
- AI reads task list, starts with first sub-task
- After finishing each sub-task, checks off box `[x]` in TASKS.md, then pauses
- User types "yes" to proceed — catches errors early before they compound

### Workflow 2: Extending Cursor with MCPs

MCPs = APIs that let an LLM safely interact with other software.

**Example: Browserbase for browser automation**
- Configure MCP servers in Cursor settings
- Issue natural language commands: "navigate to chat p and take a screen grab"
- AI controls headless browser in the cloud
- Use cases: automated front-end testing, database queries, app interaction without leaving IDE

### Workflow 3: Mastering Context with Repo Prompt

For complex jobs requiring precise control over LLM context.

1. **Select Specific Files** in Repo Prompt desktop app — only relevant files
2. **Compose the Query** with optional "stored prompts" (e.g., "Architect" persona)
3. **Generate Full Context** — combines file contents, prompt, persona using XML tags
4. **Paste into LLM** — context-rich prompt for higher quality answers

Replaces "black box" of automatic context with "glass box" of deliberate, precise control.

### Key Resources

- [Ryan Carson's rule files on GitHub](https://github.com/snarktank/ai-dev-tasks)
- [Repo Prompt](https://repoprompt.com/)
- [Browserbase](https://browserbase.com/)
- [Stagehand MCP](https://docs.stagehand.dev/integrations/mcp-server)
- [Watch on YouTube](https://youtu.be/fD4ktSkNCw4)
