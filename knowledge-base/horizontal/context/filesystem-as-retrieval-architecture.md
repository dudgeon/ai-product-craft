---
created: 2026-02-14
updated: 2026-02-14
template: templates/knowledge-entry.md
template_version: 4
tags: [knowledge, ai-pm, mental-model, context-engineering, filesystem, retrieval, git]
status: draft
entry_type: mental-model
origin: sourced
featured: false
domain: horizontal
horizontal_domain: context
project: ai-pm
---

# Filesystem as Retrieval Architecture

## Summary

Well-structured markdown in a git repo, navigated with filesystem primitives, is a legitimate retrieval system — not a stopgap until you get "real" infrastructure. The filesystem *is* the database. Directory hierarchy is the index. Frontmatter is the metadata layer. Git history is the temporal layer. `grep` is the query engine.

This mental model is distinct from "filesystem as agent state" (which is about where state lives). This is about how agents *find and navigate* knowledge. The key insight: every structural decision in a knowledge repository — folder names, file naming conventions, frontmatter fields, README content — is a retrieval decision. The agent discovering your knowledge base doesn't have a search bar; it has `ls`, `find`, `grep`, and `head`. The structure must be optimized for those tools.

Letta's Context Repositories validate this empirically: agents clone a git-backed filesystem, use standard terminal tools (`cat`, `grep`, `find`) to read, write, and reorganize memory, and git provides free temporal tracking without graph database infrastructure. Critically, no embedding search or MCP is required — the pattern is portable across any agent that can read files.

## How to Apply

**When to use**: When designing knowledge systems for coding agents, when choosing between filesystem-only and infrastructure-heavy approaches, or when evaluating whether to invest in embedding search or graph databases. This model clarifies what you get for free from good filesystem structure.

**When not to use**: At scale (thousands of documents) where semantic search genuinely outperforms grep, or when the query patterns require multi-hop reasoning across entities that don't co-locate in the directory tree.

**Design implications**:
1. **Directory structure = layer 1 index**: Folder names and hierarchy must be optimized for scannability, not just human aesthetics. Descriptive folder names matter more than short ones. An agent running `ls domains/` gets the navigational index for free.
2. **Frontmatter = layer 2 metadata**: YAML frontmatter with summaries, types, and tags provides the intermediate retrieval layer. An agent can `head -20` to read frontmatter without loading the full file.
3. **Git history = temporal layer**: `git log --oneline -- path/to/file` gives the temporal history of any entity. `git log --diff-filter=M --name-only` shows what changed and when. Zero-infrastructure temporal tracking.
4. **READMEs = curated manifests**: Each directory's README serves as a human-and-agent-readable guide to what's inside, highlighting what matters rather than listing everything.
5. **Semantic search is acceleration, not architecture**: If your MCP server or embedding database goes down, an agent with filesystem access should still navigate effectively. The filesystem conventions are the primary retrieval architecture; search layers accelerate it.

**For AI PMs**: This model is liberating for enterprise contexts. You don't need to wait for IT to approve an MCP server or embedding database. The pattern works today, in any agent that can read files. The graduation path to richer retrieval is available when the organization is ready, but the baseline is fully functional with zero infrastructure beyond a git repo.

## Sources

### From: [2026-02-14 Progressive Disclosure & Context Graphs](../../sources/2026-02-14-progressive-disclosure-context-graphs.md)
**Key quote**: "Well-structured markdown in a git repo, navigated with filesystem primitives, is a legitimate retrieval system — not just a stopgap until you get 'real' infrastructure."
**Attribution**: Research synthesis, primarily drawing on Letta's Context Repositories (Feb 2026)
**What this source adds**: Validates the filesystem-only approach by surveying Letta's production implementation (agents clone repos, use terminal tools, git provides temporal tracking). Also establishes the principle that semantic search should be treated as an acceleration layer on top of filesystem conventions, not a replacement for them.
**Links**: [Letta Blog Post](https://www.letta.com/blog/context-repositories) | [Archive](../../sources/2026-02-14-progressive-disclosure-context-graphs.md)

## Related

- [Filesystem as Agent State](../agents/skills/filesystem-as-agent-state.md) — Complementary mental model. Agent state is about *what exists*; retrieval architecture is about *how agents find it*. Together they describe the full filesystem-centric agent architecture.
- [Three-Layer Context Disclosure](three-layer-context-disclosure.md) — The filesystem naturally implements three-layer disclosure: directory structure (layer 1), frontmatter (layer 2), file content (layer 3).
- [Deliberate Context Selection](deliberate-context-selection.md) — Filesystem structure determines what's discoverable; deliberate selection determines what gets loaded into the context window.
