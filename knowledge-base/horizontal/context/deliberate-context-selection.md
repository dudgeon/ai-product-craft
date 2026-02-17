---
created: 2026-02-07
updated: 2026-02-14
template: templates/knowledge-entry.md
template_version: 3
tags: [knowledge, ai-pm, technique, context-engineering]
status: draft
entry_type: technique
origin: sourced
featured: false
domain: horizontal
horizontal_domain: context
project: ai-pm
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

### From: [2026-02-07 Ryan Carson Structured AI Development](../../sources/2026-02-07-ryan-carson-structured-ai-development.md)
**Key quote**: Repo Prompt "replaces the 'black box' of automatic context with the 'glass box' of deliberate, precise control."
**Attribution**: Ryan Carson
**What this source adds**: Carson demonstrates this through Repo Prompt — a desktop app that lets you visually select files, add persona instructions, and generate structured prompts with XML tags. The key distinction: automatic context is fine for routine work, but for complex tasks you need surgical precision over what the LLM sees.
**Links**: [Original](https://www.chatprd.ai/how-i-ai/ryan-carsons-3-step-playbook-for-structured-ai-development-in-cursor) | [Archive](../../sources/2026-02-07-ryan-carson-structured-ai-development.md)

### From: [2026-02-08 Getting Paid to Vibe Code](../../sources/2026-02-08-vibe-coding-new-ai-job.md)
**Key quote**: "Think of it like a genie granting you three wishes. Every request consumes tokens for reading, thinking, and executing."
**Attribution**: Lazar Jovanovic (via Lenny Rachitsky)
**What this source adds**: The "genie and three wishes" metaphor reframes context selection from a technical concern (which files to include) to a resource allocation problem (how to spend limited context window budget). Jovanovic's point: vague requests waste the majority of tokens on disambiguation, leaving little capacity for quality output. This complements Carson's "glass box" framing — Carson focuses on *what* goes in, Jovanovic on *what it costs*.
**Links**: [Original](https://www.lennysnewsletter.com/p/getting-paid-to-vibe-code) | [Archive](../../sources/2026-02-08-vibe-coding-new-ai-job.md)

## Related

- [Context First Development](../../product-lifecycle/build/context-first-development.md)
- [Interactive PRD Writing](../../product-lifecycle/build/interactive-prd-writing.md)
- [Be 100x More Specific](../prompting/be-100x-more-specific.md)
- [Structured Context Loading](../agents/system-design/structured-context-loading.md) — The systematic version: purpose-built files designed to be loaded before each interaction
