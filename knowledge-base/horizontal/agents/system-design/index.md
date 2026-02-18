---
created: 2026-02-16
updated: 2026-02-16
tags: [index, ai-pm, horizontal, agents, system-design]
status: active
domain: horizontal
horizontal_domain: agents
project: ai-pm
---

# Agent System Design

Patterns, techniques, and mental models for designing and configuring agent systems — organized by the domain of practice they belong to. Applies regardless of which harness (Claude Code, Cursor, Devin, etc.) you use.

## Sub-domains

### [Instruction Design](instruction-design/) — CLAUDE.md, agents.md & Behavioral Configuration

The practice of defining agent behavior through persistent markdown instruction files.

- [Structured Context Loading](instruction-design/structured-context-loading.md) — Purpose-built files loaded before each interaction to align agent behavior
- [Knowledge Capture as Side Effect](instruction-design/knowledge-capture-as-side-effect.md) — Design agent systems so knowledge capture is a byproduct of corrections `solid`

### [Skills](skills/) — Discrete Agent Capabilities

Reusable, composable agent procedures packaged as files. How to design, bootstrap, and scale them.

- [Meta-Skill Pattern](skills/meta-skill-pattern.md) — Build a "skill that builds skills" to bootstrap agent capabilities consistently

### [Supervision](supervision/) — Human Governance of Agent Execution

Patterns for staying in control without micromanaging — approval gates, execution pacing, capability gating, and behavioral observation.

- [Stepwise Task Execution](supervision/stepwise-task-execution.md) — One-task-at-a-time execution with pause-and-approve checkpoints
- [Progressive Tool Disclosure](supervision/progressive-tool-disclosure.md) — Revealing MCP tools in layers to combat choice paralysis and hallucination
- [Agent-Mediated Self-Reflection](supervision/agent-mediated-self-reflection.md) — Using agents to observe behavioral patterns from digital exhaust

### [Architecture](architecture/) — Structural Foundations

Where state lives, how agents connect to external systems, what the chassis looks like.

- [Filesystem as Agent State](architecture/filesystem-as-agent-state.md) — Agent architecture = filesystem (state) + LLM (orchestrator)
- [Agent as Cross-Tool Workflow Hub](architecture/agent-as-cross-tool-workflow-hub.md) — Local agent + MCP integrations as orchestration layer

---

[← Back to Agents](../)
