---
created: 2026-02-14
updated: 2026-02-22
template: templates/knowledge-entry.md
template_version: 4
tags: [knowledge, ai-pm, technique, context-engineering, progressive-disclosure, retrieval]
status: draft
entry_type: technique
origin: sourced
featured: false
domain: horizontal
horizontal_domain: context
project: ai-pm
---

# Three-Layer Context Disclosure

## Summary

Multiple independent implementations have converged on a common pattern for delivering knowledge to agents: expose information in three layers of increasing detail, letting the agent decide what to fetch at each stage rather than dumping everything upfront.

- **Layer 1 — Index/Map (~50-100 tokens per item)**: Lightweight metadata — titles, dates, types, token cost estimates. The agent scans this to understand *what exists* without paying the cost of *reading it all*. Think table of contents, not the book.
- **Layer 2 — Summaries (~200-500 tokens per item)**: 2-3 sentence summaries, section headers, or chronological context. Enough to assess relevance with confidence before committing to full retrieval.
- **Layer 3 — Full Content (~500-1,000+ tokens per item)**: Complete documents, retrieved only for items the agent has determined are relevant through layers 1-2.

The technique achieves roughly 10x token savings compared to "dump everything" approaches. The core insight: filtering before fetching is dramatically more efficient than fetching then ignoring. LLMs suffer from context rot — as token count increases, the model's ability to accurately recall and follow instructions from that context decreases. Good context engineering means finding the smallest possible set of high-signal tokens that maximize the likelihood of a desired outcome.

## How to Apply

**When to use**: Any system where an agent needs to access a knowledge base, document collection, or memory store that exceeds what fits comfortably in a context window. This applies to coding agent memory, personal knowledge management, team documentation, and enterprise knowledge retrieval.

**When not to use**: When the total corpus is small enough to load entirely without attention degradation, or when the latency of multi-step retrieval is unacceptable for the use case.

**Implementation patterns**:
1. **MCP-based (Claude-Mem pattern)**: Dedicated tools for each layer — `search` returns compact index with IDs and token estimates, `get_observations` returns full details for selected IDs only. Each observation carries a type emoji and token cost in the index view for cost/relevance tradeoffs.
2. **Filesystem-based (Letta pattern)**: Directory structure is layer 1 (agent runs `ls` or `find`), YAML frontmatter with summaries is layer 2 (agent reads first 20 lines), full file content is layer 3. No external infrastructure required.
3. **Hybrid (Claude Code pattern)**: CLAUDE.md files loaded upfront as always-available context, while `glob` and `grep` provide just-in-time filesystem exploration. Skills use lightweight YAML descriptions (~100 tokens) in the system prompt; the agent reads the full SKILL.md only when relevant.
4. **Tool discovery (Strata pattern)**: Applied to tool selection rather than knowledge — Intent → Server Categories → Category Actions → Action Details → Execute. Each step only reveals what's needed for the next decision.

**For AI PMs**: This technique directly informs RAG system design, agent memory architecture, and any product where an AI needs to navigate a knowledge corpus. The key product decision is where to draw the layer boundaries — what metadata goes in the index, what goes in summaries, and what requires full retrieval. Getting this wrong (too much in layer 1, too little in layer 2) degrades both performance and cost.

## Sources

### From: [2026-02-14 Progressive Disclosure & Context Graphs](../../sources/2026-02-14-progressive-disclosure-context-graphs.md)
**Key quote**: "Filtering before fetching is dramatically more efficient than fetching then ignoring."
**Attribution**: Research synthesis citing Claude-Mem, Letta, Inferable.ai, Will Larson, Klavis Strata, and Anthropic's context engineering guidance
**What this source adds**: Surveys multiple independent implementations that converge on this pattern, identifies the three layers as a consensus architecture, and provides concrete token budget estimates per layer. Also documents the Inferable.ai finding that giving LLMs more context often makes them *worse* at instruction-following — the counterintuitive result that motivates the technique.
**Links**: [Archive](../../sources/2026-02-14-progressive-disclosure-context-graphs.md)

### From: [2026-02-13 Harness Engineering Leveraging Codex](../../sources/2026-02-13-harness-engineering-leveraging-codex.md)
**Key quote**: "Give Codex a map, not a 1,000-page instruction manual."
**Attribution**: Ryan Lopopolo, OpenAI
**What this source adds**: Production validation of the three-layer pattern at scale (~1M lines, ~1,500 PRs). OAI's AGENTS.md (~100 lines) serves as a table of contents pointing to a structured docs/ directory — a direct implementation of layer 1 (map) pointing to layer 2/3 (docs). They explicitly document why the monolithic approach fails: it crowds out the task, turns non-guidance when everything is "important," rots instantly, and resists mechanical verification. Their mitigation includes dedicated linters and CI jobs that validate the knowledge base is cross-linked and up to date — a novel enforcement layer on top of the disclosure pattern.
**Links**: [Original](https://openai.com/index/harness-engineering/) | [Archive](../../sources/2026-02-13-harness-engineering-leveraging-codex.md)

## Related

- [Deliberate Context Selection](deliberate-context-selection.md) — Three-layer disclosure is the system-level version of deliberate context selection. One is the architecture; the other is the individual practice.
- [Filesystem as Retrieval Architecture](filesystem-as-retrieval-architecture.md) — The filesystem implementation of three-layer disclosure, where directory structure = layer 1, frontmatter = layer 2, file content = layer 3.
- [Context First Development](../../product-lifecycle/build/context-first-development.md) — The principle that context comes before action; three-layer disclosure is a technique for delivering that context efficiently.
