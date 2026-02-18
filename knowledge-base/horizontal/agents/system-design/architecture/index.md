---
created: 2026-02-16
updated: 2026-02-16
tags: [index, ai-pm, horizontal, agents, system-design, architecture]
status: active
domain: horizontal
horizontal_domain: agents
project: ai-pm
---

# Architecture — Structural Foundations

The underlying structural model: where state lives, how agents connect to external systems, what the chassis looks like independent of instructions or skills. Decisions you make *before the agent runs*.

## Entries

- [Filesystem as Agent State](filesystem-as-agent-state.md) — Agent architecture = filesystem (state) + LLM (orchestrator); company-as-filesystem gives agents a shared namespace
- [Agent as Cross-Tool Workflow Hub](agent-as-cross-tool-workflow-hub.md) — Local agent + MCP integrations replaces manual cross-tool workflows; becomes the orchestration layer across disconnected SaaS tools

---

[← Back to System Design](../)
