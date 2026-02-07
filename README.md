---
created: 2026-02-05
updated: 2026-02-07
tags: [project, ai-pm-craft, product-management, learning]
status: active
domain: professional-development
---

# AI Product Management Craft

A structured learning project to level up as a product manager in the AI/LLM era, and to be able to explain the concepts to others.

## Goal

Build a deep, well-sourced body of knowledge about AI product management — from techniques and mental models to insights about what separates great AI PMs from the rest. Every idea should be traceable back to its sources with quotes, context, and links.

## How This Works

### Source Lifecycle

```
Discover → Capture (unread) → Read → Process → Knowledge Base
```

1. **Discover**: Find an article, video, newsletter, tweet thread
2. **Capture**: Drop in `inbox/` with `project: ai-pm-craft` tag, or create directly in `sources/`
3. **Read**: Mark as `reading` → `read`, add summary and notes
4. **Process**: Extract discrete ideas into knowledge entries with source lineage
5. **Synthesize**: Knowledge entries accumulate citations from multiple sources over time

### Source Files (`sources/`)

Each source is a markdown file with archived content, reading status, and extracted ideas. See `templates/source.md`.

**Status lifecycle**: `unread` → `reading` → `read` → `processed`

### Knowledge Entries (`knowledge/`)

Synthesized ideas organized by type. Each entry is atomic — one idea per file — and tracks lineage back to every source that discusses it. See `templates/knowledge-entry.md`.

**Status lifecycle**: `draft` → `solid` → `canonical`

**Entry types**: `technique`, `mental-model`, `insight`

---

## Knowledge Map

*The table of contents for all knowledge entries, organized by topic hierarchy. Updated as new entries are created or restructured.*

### Strategy & Vision

*How to set direction for AI products, evaluate opportunities, and make bets.*

### Shipping & Execution

*How to move AI products from idea to production — scoping, tradeoffs, iteration.*

- [[prd-driven-ai-development]] — Three-file rule system for structured AI development: PRD → tasks → stepwise execution with human-in-the-loop
- [[context-first-development]] — "Slow down to speed up" — the biggest mistake in AI-assisted development is rushing past context

### Evaluation & Measurement

*How to measure AI product quality, define success metrics, handle non-determinism.*

### User Experience & Design

*Patterns for AI-powered interfaces, managing user expectations, trust calibration.*

### Technical Fluency

*What AI PMs need to understand about models, infra, evals, and the stack — without becoming engineers.*

- [[deliberate-context-selection]] — Hand-picking files for LLM context ("glass box") vs. relying on automatic context ("black box")

### Stakeholder & Team Dynamics

*Working with ML engineers, researchers, executives. Communicating uncertainty. Building trust.*

- [[scale-manager-expertise-with-ai]] — Automate "0-to-60%" repetitive feedback so managers can focus on deep strategic thinking and mentorship
- [[reverse-engineer-judgment-into-ai]] — Collect before/after examples, have AI discover your implicit criteria, encode into reusable evaluator

### Career & Growth

*PM career progression, skill development, differentiation in the AI era.*

- [[ai-as-writing-coach]] — Structured workflow for using AI to sharpen written communication: thesis validation → blind spots → restructuring

### Uncategorized

*Knowledge entries not yet placed in the hierarchy. Review periodically and refile.*

---

## Reading Queue

*Quick view of source status. For full details, see `sources/_index.md`.*

### Currently Reading

*None yet.*

### Up Next (Unread)

- [[2026-02-05-teresa-torres-claude-code-task-management]] — Teresa Torres's Claude Code workflows for task management, research automation, and context libraries (article, Claire Vo / ChatPRD)
- [[2026-02-06-git-workflows-agentic-era]] — Git subtree/submodule patterns for sharing context across repos in the agentic era (article, organic)
- [[2026-02-06-spec-driven-development-no-code-library]] — A software library with no code: spec-only libraries and when they work (article, Drew Breunig)
- [[2026-02-06-build-ai-product-sense]] — Using Cursor for non-technical work to build AI product sense — RAG, memory, context engineering (newsletter, Tal Raviv & Aman Khan / Lenny's)
- [[2026-02-06-brex-agent-human-ops]] — How Brex redesigns operations with AI: 3-level ops model, agent platform, generalist hiring (article, First Round)
- [[2026-02-06-agent-native-engineering]] — Restructuring engineering orgs around agents as ICs: task levels, code review, token spend (article, Andrew Pignanelli)
- [[2026-02-06-teresa-torres-claude-code-guide]] — Claude Code for non-technical people: comparison with browser/desktop, data portability (article, Teresa Torres / Product Talk)
### Recently Processed

- [[2026-02-07-ryan-carson-structured-ai-development]] → [[prd-driven-ai-development]], [[context-first-development]], [[deliberate-context-selection]]
- [[2026-02-07-hilary-gridley-scaling-yourself-custom-gpts]] → [[reverse-engineer-judgment-into-ai]], [[ai-as-writing-coach]], [[scale-manager-expertise-with-ai]]

---

## Progress Log

### 2026-02-07
- Inbox triage: 11 items processed, 8 unique sources added (4 Ryan Carson duplicates merged)
- Processed Ryan Carson source → 3 knowledge entries (prd-driven-ai-development, context-first-development, deliberate-context-selection)
- Processed Hilary Gridley source → 3 knowledge entries (reverse-engineer-judgment-into-ai, ai-as-writing-coach, scale-manager-expertise-with-ai)
- 6 knowledge entries created, Knowledge Map updated

### 2026-02-05
- Project structure created
- Templates defined: `source.md`, `knowledge-entry.md`
- First source captured: Teresa Torres / Claire Vo article on Claude Code workflows
- Processing workflows documented

---

## Related

- [[professional-development]] — Parent domain
- Context: `context/professional.md`
- Decision: [[008-source-to-knowledge-pattern]]

---

[← Back to Professional Development](../README.md)
