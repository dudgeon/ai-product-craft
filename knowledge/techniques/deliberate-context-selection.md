---
created: 2026-02-07
updated: 2026-02-07
template: templates/knowledge-entry.md
template_version: 1
tags: [knowledge, ai-pm-craft, technique, context-engineering]
status: draft
entry_type: technique
domain: professional-development
project: ai-pm-craft
---

# Deliberate Context Selection

## Summary

When working with LLMs on complex tasks (architectural reviews, tricky refactors, cross-cutting changes), the quality of output depends heavily on which files and information the model can see. Automatic context selection (what an IDE guesses you need) works for simple tasks but introduces noise or misses critical files for complex ones. Deliberate context selection means hand-picking exactly which files, schemas, and instructions the LLM receives — replacing the "black box" of automatic context with a "glass box" of precise, intentional control.

## How to Apply

**When to use**: Complex tasks where context quality matters more than speed — architectural decisions, multi-file refactors, tasks requiring understanding of specific schemas or APIs.

**When not to use**: Simple single-file edits where automatic context is sufficient.

**Approaches**:
1. **Tool-assisted selection**: Use tools like Repo Prompt to visually select specific files, compose queries with persona instructions, and generate structured prompts with XML tags separating file contents from user instructions
2. **Manual curation**: In Cursor, use @-mentions to explicitly include specific files. In Claude Code, reference specific files by path
3. **Persona layering**: Add "stored prompts" like an "Architect" persona that shapes how the AI reasons about the selected context

**For AI PMs**: This is a direct parallel to RAG system design. The question "what context should this AI feature have access to?" is the same whether you're building a personal workflow or a production system. Understanding deliberate context selection builds intuition for retrieval quality, context window tradeoffs, and the difference between "has access to" and "is paying attention to."

## Sources

### From: [[2026-02-07-ryan-carson-structured-ai-development]]
**Key quote**: Repo Prompt "replaces the 'black box' of automatic context with the 'glass box' of deliberate, precise control."
**What this source adds**: Carson demonstrates this through Repo Prompt — a desktop app that lets you visually select files, add persona instructions, and generate structured prompts with XML tags. The key distinction: automatic context is fine for routine work, but for complex tasks you need surgical precision over what the LLM sees.
**Links**: [Original](https://www.chatprd.ai/how-i-ai/ryan-carsons-3-step-playbook-for-structured-ai-development-in-cursor) | [[2026-02-07-ryan-carson-structured-ai-development|Archive]]

## Related

- [[context-first-development]]
- [[prd-driven-ai-development]]
