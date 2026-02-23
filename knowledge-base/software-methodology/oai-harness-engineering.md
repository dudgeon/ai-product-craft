---
created: 2026-02-22
updated: 2026-02-22
template: templates/knowledge-entry.md
template_version: 5
tags: [knowledge, ai-pm, mental-model, swe-methodology, agent-first, harness-engineering, codex]
status: draft
entry_type: mental-model
origin: sourced
featured: false
domain: software-methodology
project: ai-pm
---

# OAI Harness Engineering

## Summary

A distinct software engineering methodology where humans write zero code and agents generate everything — application logic, tests, CI, tooling, documentation, observability, and internal developer utilities. OpenAI's team shipped an internal product (~1M lines, ~1,500 PRs, 3 engineers growing to 7) over 5 months using this approach with Codex. The constraint was intentional: by refusing to write code manually, the team was forced to discover what infrastructure enables agent velocity at scale.

The methodology redefines the engineer's role: the primary job is not writing code but designing environments, specifying intent, and building feedback loops that allow agents to do reliable work. When something fails, the fix is never "try harder" — it's "what capability is missing, and how do we make it both legible and enforceable for the agent?" This shifts engineering from an execution discipline to an environmental design discipline.

Five defining characteristics distinguish harness engineering from adjacent approaches (vibe coding, compound engineering, spec-driven development):

1. **Deliberate constraint**: Zero manually-written code is a forcing function, not an aspiration. It exposes which engineering investments actually matter for agent effectiveness.
2. **Repository as system of record**: Anything not in the repo is invisible to agents. Slack discussions, Google Docs, tribal knowledge — all illegible. Knowledge must be versioned, indexed, and discoverable via filesystem primitives.
3. **Mechanical enforcement over documentation**: Architecture constraints are enforced by custom linters and structural tests, not by hoping agents read the docs. Linter error messages are designed as remediation instructions injected directly into agent context.
4. **Continuous entropy management**: Recurring background agents scan for drift, grade quality, and open targeted refactoring PRs — functioning as garbage collection for an agent-generated codebase.
5. **Progressive autonomy**: The team incrementally expanded what agents could do end-to-end — from single PRs to full feature cycles (reproduce bug → fix → video proof → PR → respond to feedback → merge).

## How to Apply

**When to reference this model**: When evaluating how AI transforms engineering methodology at the team or org level. This is a real case study of what happens when you push "agents write code" to its logical extreme — and what infrastructure investments it demands.

**Key insight for AI PMs**: The engineering bottleneck shifts from code throughput to human QA capacity. As agent output scales, the scarce resource becomes human attention for validation, not coding time. Products built this way need to invest heavily in making application state (UI, logs, metrics) directly legible to agents — not just to humans.

**Comparison to other methodologies**:

| Methodology | Human role | Agent role | Code authorship |
|---|---|---|---|
| Traditional SWE | Write code, review code | Autocomplete, suggestions | 100% human |
| Vibe coding | Prompt and iterate | Generate, refine | Mostly agent, human edits |
| Compound engineering | Architect, prompt, review | Generate per spec | Agent generates, human reviews |
| Spec-driven development | Write specs and tests | Generate implementation | Agent generates to spec |
| **Harness engineering** | Design environments, specify intent | Generate everything | 100% agent |

**What makes it work** (prerequisites):
- Rigid architectural model with mechanically enforced layer boundaries
- AGENTS.md as lightweight table of contents (~100 lines), not encyclopedia
- Structured docs/ directory as the knowledge system of record
- Application bootable per git worktree for agent-local instances
- Observability stack (logs, metrics, traces) exposed to agents via query interfaces
- Browser automation wired into agent runtime (CDP for DOM snapshots, screenshots)
- Recurring cleanup agents that enforce "golden principles" on a schedule

**What to watch**: The team acknowledges they don't yet know how architectural coherence evolves over years in a fully agent-generated system. The approach works at the scale of a 5-month internal product with 7 engineers — long-term maintainability at larger scale is unproven.

## Sources

### From: [2026-02-13 Harness Engineering Leveraging Codex](../../sources/2026-02-13-harness-engineering-leveraging-codex.md)
**Key quote**: "Humans steer. Agents execute."
**Attribution**: Ryan Lopopolo, OpenAI
**What this source adds**: The definitive case study — the only public account of a team shipping a real product with zero manually-written code at meaningful scale. Provides concrete numbers (1M lines, 1,500 PRs, 3.5 PRs/engineer/day), specific architectural patterns (layer model, linter enforcement), and honest assessment of what remains unknown.
**Links**: [Original](https://openai.com/index/harness-engineering/) | [Archive](../../sources/2026-02-13-harness-engineering-leveraging-codex.md)

## Related

- [Spec-Driven Development](../adjacent-disciplines/spec-driven-development.md) — Adjacent methodology where specs + tests replace code; harness engineering goes further by having agents generate everything including specs and tests
- [Compound Engineering Loop](compound-engineering-loop.md) — Related methodology; compound engineering's four-step loop is compatible with harness engineering's zero-code constraint
- [Mechanical Architecture Enforcement for Agents](../horizontal/agents/system-design/architecture/mechanical-architecture-enforcement.md) — The enforcement technique that makes harness engineering viable at scale
- [Agent Entropy Management](../horizontal/agents/system-design/supervision/agent-entropy-management.md) — The maintenance pattern that keeps agent-generated codebases coherent over time
- [Three-Layer Context Disclosure](../horizontal/context/three-layer-context-disclosure.md) — The context pattern OAI uses (AGENTS.md as map, docs/ as system of record)
- [Filesystem as Retrieval Architecture](../horizontal/context/filesystem-as-retrieval-architecture.md) — The repo-as-system-of-record principle that underpins the methodology
- [Intentional Understaffing for AI-First Teams](../../ai-adoption/intentional-understaffing-ai-first-teams.md) — Related adoption pattern; OAI's 3-engineer team is an extreme version of deliberate understaffing
