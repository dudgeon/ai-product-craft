---
created: 2026-02-22
updated: 2026-02-22
template: templates/knowledge-entry.md
template_version: 5
tags: [knowledge, ai-pm, technique, agents, supervision, entropy, cleanup, technical-debt]
status: draft
entry_type: technique
origin: sourced
featured: false
domain: horizontal
horizontal_domain: agents
project: ai-pm
---

# Agent Entropy Management

## Summary

Agent-generated codebases accumulate entropy faster than human-written ones because agents replicate patterns that already exist in the repository — including suboptimal or inconsistent ones. Left unchecked, this drift compounds. OpenAI's harness engineering team initially spent 20% of engineering time (every Friday) manually cleaning up "AI slop." That didn't scale.

The solution: encode "golden principles" directly into the repository and build a recurring cleanup process that runs as background agent tasks. On a regular cadence, dedicated Codex agents scan the codebase for deviations from golden principles, update quality grades per domain, and open targeted refactoring PRs. Most of these PRs can be reviewed in under a minute and automerged.

This functions as garbage collection for a codebase. The core insight: technical debt is a high-interest loan — continuous small payments are almost always better than letting it compound into painful bursts. Human taste is captured once (as golden principles and quality standards), then enforced continuously by agents on every line of code.

## How to Apply

**When to use**: Any codebase with significant agent-generated code. The technique becomes essential as agent throughput increases — more generated code means faster drift accumulation.

**When not to use**: Early-stage prototypes where patterns haven't stabilized yet. You need established golden principles before you can enforce them.

**Implementation steps**:

1. **Define golden principles**: Opinionated, mechanical rules that keep the codebase legible and consistent for future agent runs. Examples: prefer shared utility packages over hand-rolled helpers (centralize invariants), validate data at boundaries instead of probing YOLO-style, structured logging over ad-hoc console output.
2. **Create quality grades**: Score each product domain and architectural layer against the golden principles. Track grades over time to detect drift direction.
3. **Build recurring cleanup tasks**: Schedule background agent runs that scan for deviations. These agents should be narrowly scoped — one task per golden principle — so their output is reviewable in under a minute.
4. **Open targeted refactoring PRs**: Each cleanup run produces small, focused PRs that address specific deviations. Avoid large "cleanup everything" PRs — they're harder to review and more likely to introduce regressions.
5. **Automerge when safe**: For well-tested cleanups (formatting, naming, import reorganization), enable automerge. Reserve human review for structural changes.
6. **Capture taste continuously**: When human reviewers identify new bad patterns, encode the fix as a golden principle and add it to the cleanup rotation. The system improves with every review comment.

**The escalation path**: Review comments → documentation updates → golden principles → recurring cleanup agents → structural linters. Each level increases the radius and permanence of enforcement.

## Sources

### From: [2026-02-13 Harness Engineering Leveraging Codex](../../sources/2026-02-13-harness-engineering-leveraging-codex.md)
**Key quote**: "Technical debt is like a high-interest loan: it's almost always better to pay it down continuously in small increments than to let it compound and tackle it in painful bursts."
**Attribution**: Ryan Lopopolo, OpenAI
**What this source adds**: The concrete pattern of recurring background agents as garbage collectors, the "20% of time cleaning AI slop" problem that motivated it, and the golden principles concept. Also the key finding that human taste is captured once and then enforced continuously — a leverage pattern.
**Links**: [Original](https://openai.com/index/harness-engineering/) | [Archive](../../sources/2026-02-13-harness-engineering-leveraging-codex.md)

## Related

- [OAI Harness Engineering](../../../software-methodology/oai-harness-engineering.md) — The methodology where this technique is essential; without entropy management, harness engineering produces unmaintainable codebases
- [Mechanical Architecture Enforcement for Agents](../architecture/mechanical-architecture-enforcement.md) — Complementary technique: enforcement prevents new violations, entropy management fixes existing drift
- [Knowledge Capture as Side Effect](../instruction-design/knowledge-capture-as-side-effect.md) — Related pattern where corrections become persistent system knowledge; entropy management is the codebase equivalent
