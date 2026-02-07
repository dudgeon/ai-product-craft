---
created: 2026-02-06
updated: 2026-02-07
template: templates/source.md
template_version: 2
tags: [source, ai-pm-craft, product-sense, cursor]
status: unread
source_type: newsletter
source_url: "https://www.lennysnewsletter.com/p/how-to-build-ai-product-sense"
archive_url: "domains/professional-development/ai-pm-craft/sources/2026-02-06-build-ai-product-sense.md"
author: "Tal Raviv, Aman Khan"
published: 2026-02-03
discovered: 2026-02-06
summary: "PMs build AI product sense by using coding agents (Cursor, Claude Code) for non-technical daily work — strategy, prioritization, data analysis. Hands-on exposure to tool calling, RAG, context windows, and context rot builds intuition that reading about AI can't. Includes step-by-step tutorial building a personal productivity OS in Cursor."
domain: professional-development
project: ai-pm-craft
---

# How to Build AI Product Sense

**By**: Tal Raviv, Aman Khan
**Source**: [Lenny's Newsletter](https://www.lennysnewsletter.com/p/how-to-build-ai-product-sense)
**Type**: newsletter

## Summary

*Fill after reading. 2-3 sentences: what is this about, what's the core argument or insight?*

## Key Ideas Extracted

*Fill during processing. Each idea links to a knowledge entry.*

## Notes

*Your annotations, reactions, questions, disagreements. Written during or after reading.*

## Raw Content

**Core thesis**: The single most transformative habit to internalize important AI concepts is to move away from consumer-grade UIs (ChatGPT, Granola, Lovable) and into more powerful AI coding agents like Cursor and Claude Code. Getting hands dirty with coding agents helps build "AI product sense"—the ability to correctly anticipate what will be truly impactful for users and also feasible with AI.

AI product sense is encountering support tickets about AI "forgetting" facts and recognizing it as context rot. Or watching a user struggle through a workflow and confidently saying that agent memory solves this—and knowing how to restructure the experience.

**10-Step Tutorial Structure**:

**Steps 1-4: Get Set Up and Familiar with Cursor**
- Download Cursor (desktop app, not web version)
- Create a new project
- Continue the post inside Cursor itself (Magic School Bus inspired)
- Create a Disney song parody to learn basics (Agent mode, file editing, Keep/Undo)

**Key insight from Step 3**: Cursor is just three familiar tools combined:
1. ChatGPT (chat interface)
2. A text editor
3. File explorer

Or as one student said: "AI that can touch any file on my computer."

**Steps 5-6: Hands-on with AI Models and Tool Calls**
- **Step 5: Model Selection** — Try same query across multiple models to build intuition. Claude models sensitive to copyright; OpenAI models stumbled with apply_patch tool. Key lesson: "There are only a few frontier LLMs, and they're available to all product teams. Innovation is how we apply them."
- **Step 6: Tool Calls** — LLMs can only produce text; actions happen through tools. Tools are familiar operations (read_file, search_replace). Cursor is the "handyman" — LLM describes what it wants, Cursor executes. If you've heard "MCP client" or "agent harness," those describe Cursor's role.

**MCP Explained**: SaaS companies provide custom tools for LLM interaction. MCP is a standard interface so each company only needs one connector. Analogy: USB or Bluetooth. "For simplicity, MCP is just another tool the agent can use, with a standardized interface."

**Steps 7-10: Build a Personal OS**
- **Step 7: Create Personal OS** — Lightweight productivity system: Knowledge/, Tasks/, GOALS.md, AGENTS.md. The user becomes PM of their own AI product.
- **Step 8: RAG** — "Before I start talking, I gotta go look everything up and read it first." Agent searches files to provide context to LLM. Perplexity, Google AI Mode, Claude Code all use RAG.
- **Step 9: Agent Memory (AGENTS.md)** — LLMs are "Mensa geniuses with the short-term memory of a hamster." AGENTS.md is a markdown file auto-prepended to every chat. "Memory is just a text file prepended to every conversation." Memory has a cost — takes up context window space.
- **Step 10: Context Engineering** — Anytime you've dragged a file into ChatGPT, started deep research, or created project instructions, you were doing context engineering. Watch Cursor's token counter like a car's gas tank. Context rot: model performance degrades with more tokens.

**Practical difference between Cursor and ChatGPT**:
- Cursor = files as knowledge + chat as interface + instructions that always apply
- Two form-factor differences change everything: selective context (drag files into each chat) and malleable knowledge (AI edits files directly)
- In ChatGPT, value lives in conversation history; in Cursor, value lives in documents

**Key concepts covered**: AI product sense, model selection, tool calling, MCP, RAG, agent memory, context engineering, context rot, context window management.
