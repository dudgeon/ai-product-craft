---
created: 2026-02-16
updated: 2026-02-16
tags: [index, ai-pm, horizontal, agents, system-design]
status: active
domain: horizontal
horizontal_domain: agents
project: ai-pm
---

# Agent System Design — Architecture & Control Patterns

Patterns, techniques, and mental models for designing and configuring agent systems — architecture, behavior, and control mechanisms that apply regardless of which harness (Claude Code, Cursor, Devin, etc.) you use.

## Entries

- [Stepwise Task Execution](stepwise-task-execution.md) — One-task-at-a-time execution with pause-and-approve checkpoints
- [Meta-Skill Pattern](meta-skill-pattern.md) — Build a "skill that builds skills" to bootstrap agent capabilities consistently
- [Filesystem as Agent State](filesystem-as-agent-state.md) — Agent architecture = filesystem (state) + LLM (orchestrator)
- [Knowledge Capture as Side Effect](knowledge-capture-as-side-effect.md) — Design agent systems so knowledge capture is a byproduct of corrections
- [Agent as Cross-Tool Workflow Hub](agent-as-cross-tool-workflow-hub.md) — Local agent + MCP integrations as orchestration layer across disconnected SaaS tools
- [Agent-Mediated Self-Reflection](agent-mediated-self-reflection.md) — Using agents to observe behavioral patterns from digital exhaust
- [Progressive Tool Disclosure](progressive-tool-disclosure.md) — Revealing MCP tools in layers to combat choice paralysis and hallucination
- [Structured Context Loading](structured-context-loading.md) — Purpose-built files loaded before each interaction to align agent behavior

---

[← Back to Agents](../README.md)
