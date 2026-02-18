---
created: 2026-02-14
updated: 2026-02-14
template: templates/knowledge-entry.md
template_version: 4
tags: [knowledge, ai-pm, technique, agents, mcp, tool-management, progressive-disclosure]
status: draft
entry_type: technique
origin: sourced
featured: false
domain: horizontal
horizontal_domain: agents
project: ai-pm
---

# Progressive Tool Disclosure

## Summary

When agents have access to many tools (particularly via MCP), exposing all of them at once causes "choice paralysis" and hallucination — the agent struggles to select the right tool and may invent tool calls that don't exist. Progressive tool disclosure solves this by revealing tools in layers: the agent first selects an intent, then a tool category, then a specific action, then sees the action's parameters, then executes. Each step only reveals what's needed for the next decision.

Benchmark results show +15% higher accuracy versus loading all tools upfront. The pattern applies directly to MCP tool overload — a growing problem as agents gain access to more servers and capabilities. It's the tool-management equivalent of three-layer context disclosure applied to knowledge.

## How to Apply

**When to use**: When an agent has access to 20+ tools, when MCP servers expose many endpoints, or when tool selection accuracy is degrading as capabilities expand. The inflection point is typically when the agent starts hallucinating tool names or calling tools with incorrect parameters due to confusion.

**When not to use**: When the agent has a small, well-defined tool set (under ~15 tools) where the cognitive overhead of layered discovery exceeds the benefit. For simple agents with clear tool boundaries, flat tool exposure works fine.

**Implementation approaches**:
1. **Guided discovery (Strata pattern)**: Intent → Server Categories → Category Actions → Action Details → Execute. Each layer is a tool call that returns the options for the next layer. The agent never sees all tools at once.
2. **Skill-based grouping (Claude Code pattern)**: Tools are grouped into skills with brief YAML descriptions. The system prompt includes only skill summaries; the agent reads the full skill definition only when it determines one is relevant.
3. **Dynamic tool loading**: Only register tools relevant to the current task. Use the conversation context to determine which tool servers to activate.

**For AI PMs**: As agent capabilities scale (more MCP servers, more integrations), tool management becomes a product design problem. The question shifts from "what tools does the agent have?" to "how does the agent discover and select the right tool?" Progressive tool disclosure is the UX pattern for this — it's progressive disclosure applied to capabilities rather than content.

## Sources

### From: [2026-02-14 Progressive Disclosure & Context Graphs](../../../../sources/2026-02-14-progressive-disclosure-context-graphs.md)
**Key quote**: "Instead of exposing hundreds of MCP tools at once (which causes 'choice paralysis' and hallucination), Strata guides the agent through: Intent → Server Categories → Category Actions → Action Details → Execute."
**Attribution**: Research synthesis, primarily drawing on Klavis Strata benchmarks
**What this source adds**: Documents the Strata implementation and its +15% accuracy improvement. Positions tool disclosure as a parallel pattern to knowledge disclosure — same principle (reveal complexity in layers), different application domain (tools vs content).
**Links**: [Archive](../../../../sources/2026-02-14-progressive-disclosure-context-graphs.md)

## Related

- [Three-Layer Context Disclosure](../../../context/three-layer-context-disclosure.md) — The same principle applied to knowledge retrieval rather than tool selection. Both are instances of progressive disclosure.
- [Meta-Skill Pattern](../skills/meta-skill-pattern.md) — Skills are a lightweight form of tool grouping — the meta-skill pattern organizes agent capabilities into discoverable, composable units.
- [Stepwise Task Execution](stepwise-task-execution.md) — Related operational pattern: progressive tool disclosure controls what tools are visible, stepwise execution controls how they're used.
