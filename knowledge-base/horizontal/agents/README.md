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

### [System Design](system-design/) — Agent Architecture & Control Patterns

Patterns, techniques, and mental models for designing and configuring agent systems — architecture, behavior, and control mechanisms that apply regardless of which harness you use.

- [Stepwise Task Execution](system-design/stepwise-task-execution.md) — One-task-at-a-time execution with pause-and-approve checkpoints
- [Meta-Skill Pattern](system-design/meta-skill-pattern.md) — Build a "skill that builds skills" to bootstrap agent capabilities consistently
- [Filesystem as Agent State](system-design/filesystem-as-agent-state.md) — Agent architecture = filesystem (state) + LLM (orchestrator)
- [Knowledge Capture as Side Effect](system-design/knowledge-capture-as-side-effect.md) — Design agent systems so knowledge capture is a byproduct of corrections
- [Agent as Cross-Tool Workflow Hub](system-design/agent-as-cross-tool-workflow-hub.md) — Local agent + MCP integrations as orchestration layer
- [Agent-Mediated Self-Reflection](system-design/agent-mediated-self-reflection.md) — Using agents to observe behavioral patterns from digital exhaust
- [Progressive Tool Disclosure](system-design/progressive-tool-disclosure.md) — Revealing MCP tools in layers to combat choice paralysis and hallucination
- [Structured Context Loading](system-design/structured-context-loading.md) — Purpose-built files loaded before each interaction to align agent behavior

### [Harnesses](harnesses/) — Platform-Specific Knowledge

Knowledge and practices specific to individual agent platforms — setup, configuration, capabilities, best practices.

- [Cursor: Structured AI Development](harnesses/cursor-structured-ai-development.md) — Three-file rule system, @-includes, MCP config, and Repo Prompt

### [Managing Agents](managing-agents/) — The Human-Agent Management Relationship

The practice of managing AI agents as autonomous participants — deciding what to delegate, how to delegate effectively, evaluating output, and developing agents over time. Distinct from system design (building agents) and harnesses (platforms) — this is about the *relationship* between human and agent.

**Thesis**: [Talent-to-Direction Scarcity Shift](managing-agents/talent-to-direction-scarcity-shift.md) — AI inverts traditional scarcity: talent is abundant, knowing what to ask for is the bottleneck

**Task-Agent Fit** — When to delegate:
- [Delegation Decision Framework](managing-agents/task-fit/delegation-decision-framework.md) — Three-variable equation for when delegation pays off

**Delegation Craft** — How to delegate:
- [Delegation Documentation as Agent Prompts](managing-agents/delegation/delegation-documentation-as-prompts.md) — Every field's delegation docs are AI prompts; common elements pattern

**Evaluation & Feedback** — *Planned, no entries yet*

**Agent Selection & Onboarding** — *Planned, no entries yet*

---

[← Back to Knowledge Map](../../README.md)
