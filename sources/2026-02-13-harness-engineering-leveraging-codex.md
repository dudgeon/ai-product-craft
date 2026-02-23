---
title: "Harness Engineering: Leveraging Codex in an Agent-First World"
created: 2026-02-13
updated: 2026-02-22
template: templates/source.md
template_version: 3
tags: [source, ai-pm, article]
status: processed
source_type: article
source_url: "https://openai.com/index/harness-engineering/"
archive_url: "domains/professional-development/ai-pm/sources/2026-02-13-harness-engineering-leveraging-codex.md"
author: "Ryan Lopopolo"
published: 2026-02-11
discovered: 2026-02-13
summary: "OpenAI built an internal product with 0 manually-written code using Codex agents over 5 months — 1M lines, 1500 PRs, 3 engineers. Covers agent-first engineering: redefining engineer role, progressive context disclosure, repository as system of record, enforcing architecture mechanically, entropy management."
domain: professional-development
project: ai-pm
---

# Harness Engineering: Leveraging Codex in an Agent-First World

**By**: Ryan Lopopolo (OpenAI, Member of the Technical Staff)
**Type**: article
**URL**: https://openai.com/index/harness-engineering/

## Summary

OpenAI's team built and shipped an internal product with **0 lines of manually-written code** using Codex agents over 5 months. The product has ~1M lines of code, ~1,500 PRs merged, started with 3 engineers (now 7), averaging 3.5 PRs/engineer/day. Core philosophy: "Humans steer. Agents execute."

The article introduces "harness engineering" as a distinct methodology for building software at scale with coding agents. The engineer's role shifts from writing code to designing environments, specifying intent, and building feedback loops. Key pillars: progressive context disclosure (AGENTS.md as map, not manual), repository as system of record (anything not in-repo is invisible), mechanical enforcement of architecture (custom linters with agent-targeted error messages), and continuous entropy management (recurring cleanup agents as garbage collection).

## Key Ideas Extracted

- [OAI Harness Engineering](../knowledge-base/software-methodology/oai-harness-engineering.md) — The overarching methodology: zero manually-written code, humans steer/agents execute, environment design over code writing
- [Mechanical Architecture Enforcement for Agents](../knowledge-base/horizontal/agents/system-design/architecture/mechanical-architecture-enforcement.md) — Custom linters with agent-targeted error messages; rigid layer models as multipliers, not constraints
- [Agent Entropy Management](../knowledge-base/horizontal/agents/system-design/supervision/agent-entropy-management.md) — Recurring cleanup agents as garbage collection; encode taste once, enforce continuously
- [Three-Layer Context Disclosure](../knowledge-base/horizontal/context/three-layer-context-disclosure.md) (enriched) — AGENTS.md as table of contents, not encyclopedia; progressive disclosure in practice
- [Filesystem as Retrieval Architecture](../knowledge-base/horizontal/context/filesystem-as-retrieval-architecture.md) (enriched) — Repository as system of record; anything not in-repo is invisible to agents

## Notes

- Context from user: "primarily swe methodologies with a new idea/theme for OAI Harness Engineering"
- Author is Ryan Lopopolo, Member of Technical Staff at OpenAI — corrected from generic "OpenAI" attribution
- Acknowledgements: Victor Zhu and Zach Brock contributed to the post
- Particularly relevant to: agent lifecycle management, context management, software delivery methodology
- "Give Codex a map, not a 1,000-page instruction manual" — aligns with home-brain's own CLAUDE.md philosophy
- 6+ hour single agent runs while humans sleep
- Agent-to-agent review replacing human review over time
- Custom linter error messages designed to inject remediation instructions into agent context
- Throughput increases as team grows (counterintuitive — usually the opposite)
- "No manually-written code" was a deliberate constraint to force discovery of what enables agent velocity
- App bootable per git worktree so Codex could launch and drive one instance per change
- Chrome DevTools Protocol wired into agent runtime for DOM snapshots, screenshots, navigation
- "Technical debt is like a high-interest loan" — continuous small payments beat painful bursts

---

[← Back to Source Registry]()
