---
created: 2026-02-09
updated: 2026-02-16
tags: [index, ai-pm, horizontal, agents]
status: active
domain: horizontal
horizontal_domain: agents
project: ai-pm
---

# Agents — Autonomous AI Participants

Filesystem-paired, autonomous agents — lifecycle management, rules, skills, templates. How PMs select, onboard, train, give feedback to, and performance-manage AI agents.

**Stack position**: Layer 4 (highest autonomy) — agents that operate independently with their own context, tools, and decision-making.

## Sub-domains

### [Skills](skills/) — Tool-Agnostic Patterns

Patterns, techniques, and mental models for building and managing AI agents that apply regardless of which harness you use.

- [Stepwise Task Execution](skills/stepwise-task-execution.md) — One-task-at-a-time execution with pause-and-approve checkpoints
- [Meta-Skill Pattern](skills/meta-skill-pattern.md) — Build a "skill that builds skills" to bootstrap agent capabilities consistently
- [Filesystem as Agent State](skills/filesystem-as-agent-state.md) — Agent architecture = filesystem (state) + LLM (orchestrator)
- [Knowledge Capture as Side Effect](skills/knowledge-capture-as-side-effect.md) — Design agent systems so knowledge capture is a byproduct of corrections
- [Agent as Cross-Tool Workflow Hub](skills/agent-as-cross-tool-workflow-hub.md) — Local agent + MCP integrations as orchestration layer
- [Agent-Mediated Self-Reflection](skills/agent-mediated-self-reflection.md) — Using agents to observe behavioral patterns from digital exhaust
- [Progressive Tool Disclosure](skills/progressive-tool-disclosure.md) — Revealing MCP tools in layers to combat choice paralysis and hallucination
- [Structured Context Loading](skills/structured-context-loading.md) — Purpose-built files loaded before each interaction to align agent behavior

### [Harnesses](harnesses/) — Platform-Specific Knowledge

Knowledge and practices specific to individual agent platforms — setup, configuration, capabilities, best practices.

- [Cursor: Structured AI Development](harnesses/cursor-structured-ai-development.md) — Three-file rule system, @-includes, MCP config, and Repo Prompt

---

[← Back to Knowledge Map](../../README.md)
