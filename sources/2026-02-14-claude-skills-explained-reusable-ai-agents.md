---
title: "Claude Skills Explained: My Workflow for Creating Reusable AI Agents with Cursor and Claude Code"
created: 2026-02-14
updated: 2026-02-14
template: templates/source.md
template_version: 3
tags: [source, ai-pm]
status: processed
source_type: article
source_url: "https://www.chatprd.ai/how-i-ai/claude-skills-explained"
archive_url: ""
author: "Claire Vo (ChatPRD)"
published: 2026-02-14
discovered: 2026-02-14
summary: "Walkthrough of three workflows for creating Claude Skills: using Claude's built-in skill creator (educational but impractical), using Cursor + Claude Code with a meta-skill (recommended power method), and uploading zipped skills to the Claude web UI. Demonstrates a meta-skill pattern—a skill that generates other skills—and shows changelog-to-newsletter and demo-to-follow-up as concrete examples."
domain: professional-development
project: ai-pm
---

# Claude Skills Explained: My Workflow for Creating Reusable AI Agents with Cursor and Claude Code

**By**: Claire Vo (ChatPRD)
**Source**: [ChatPRD — How I AI](https://www.chatprd.ai/how-i-ai/claude-skills-explained)
**Type**: article

## Summary

Walkthrough of three workflows for creating Claude Skills — Anthropic's feature for reusable, on-demand instructions. Skills are folder-based (`SKILL.md` + supporting files), invoked by natural language, and portable between Claude Code and the web UI.

## Key Topics

### What Claude Skills Are
- Reusable micro-instructions callable in any conversation (unlike Projects, which maintain constant context)
- A skill = a folder with `SKILL.md` (YAML metadata + natural language instructions) plus optional templates, examples, scripts
- Defined in natural language; can reference local files and run Python scripts
- Uploaded as `.zip` to claude.ai or used directly via Claude Code in the skill directory

### Workflow 1: Claude's Built-in Skill Creator (Learning)
- Claude has a meta-skill for generating other skills
- Output is very detailed: decision trees, clarifying questions, keyword triggers, templates
- **Downsides**: over-generates files (12 when ~5 needed), download failed with file-not-found error
- **Value**: educational — shows what a high-quality skill structure looks like

### Workflow 2: Cursor + Claude Code (Recommended)
- Create a `claude-skills` folder, open in Cursor
- Build a **meta-skill** (`create_skill`) by giving Cursor the Anthropic Skills docs as context
- Cursor also generated a Python validation script (`validate_skill.py`) — checks YAML, file refs, structure
- Invoke the meta-skill via Claude Code to generate domain-specific skills (e.g., changelog-to-newsletter)
- Claude Code auto-discovers skills in the working directory — no special invocation needed

### Workflow 3: Uploading to Claude Web UI
- Zip the skill folder → upload to claude.ai
- Constraint: skill names must be lowercase, letters/numbers/hyphens only
- Once uploaded, skill is immediately available in chat

### Meta-Skill Pattern
- A skill whose purpose is generating other skills — a reusable factory
- Demonstrates composability: skills can invoke and build on other skills
- The recommended starting point for any skills workflow

## Key Quotes

> "Unlike Claude Projects or custom GPTs, which keep a constant context within a specific chat, Skills are tools you can call on whenever you need them."

> "When you start building small, modular skills instead of just writing one-off prompts, you can make the work you get from AI more consistent and higher quality."

## Key Ideas Extracted

- [Meta-Skill Pattern](../knowledge-base/horizontal/agents/system-design/meta-skill-pattern.md) — Build a "skill that builds skills" to bootstrap agent capabilities consistently; factory pattern for agent skill creation

## Relevance to AI PM

- **horizontal/agents**: Meta-skill pattern is a concrete example of agent skill composition and factory patterns
- **horizontal/context**: Skills as a structured approach to context management — bundling instructions, templates, and validation together
- **build**: The changelog-to-newsletter and demo-to-follow-up skills are practical examples of PM workflow automation
