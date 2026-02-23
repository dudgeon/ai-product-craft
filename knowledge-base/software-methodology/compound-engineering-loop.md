---
created: 2026-02-23
updated: 2026-02-23
template: templates/knowledge-entry.md
template_version: 5
tags: [knowledge, ai-pm, mental-model, software-methodology, compound-engineering]
status: draft
entry_type: mental-model
origin: sourced
featured: false
domain: software-methodology
project: ai-pm
---

# Compound Engineering Loop

## Summary

In traditional engineering, each feature makes the next feature harder to build — more complexity, more edge cases, more fragility. Compound engineering inverts this: each feature makes the next one *easier*. The mechanism is a four-step loop that turns every unit of engineering work into permanent institutional learning:

1. **Plan**: Agents read the codebase (including commit history), research approaches, and write a detailed implementation plan — a text document in the repo or a GitHub issue. Planning builds a shared mental model between engineer and agent. As models improve, planning shrinks for small projects.
2. **Work**: The agent reads the plan, implements it, and creates tests. Agent self-testing via browser (MCP tools like Playwright) lets the agent verify its own work visually.
3. **Assess**: The agent reviews its own work, the engineer reviews it too, and automated tools (linters, tests) run. The key addition: the agent describes "lessons learned" from each review.
4. **Compound**: Lessons from all previous steps — bugs, performance issues, edge cases, design decisions — get encoded as rules in the codebase that agents read at the start of each new task. Learnings are automatically distributed to the whole team because rules live in the repo.

Roughly 80% of compound engineering time is spent in Plan and Assess; only 20% in Work and Compound. When agents write 100% of the code, the engineer's primary job becomes planning and evaluation — not implementation.

The enabling context: Every runs five software products, each primarily built and run by one or two people. Compound engineering is what makes this scale work — without the compounding step, single-person teams would drown in accumulated complexity.

## How to Apply

**When to use**: When running any agent-driven software development workflow and you want each iteration to improve the next. Applicable at any scale, from solo developer to team.

**When not to use**: For one-off throwaway prototypes where you'll never revisit the codebase. The investment in the compound step only pays off if there's a "next loop."

**Implementation**:
1. **Start with rules files**: Create a rules/conventions file in your codebase (CLAUDE.md, .cursorrules, etc.) that agents read at session start. Seed it with your existing conventions.
2. **After each review cycle**: Ask the agent to summarize what it learned — what went wrong, what worked, what should be different next time. Append these to the rules file.
3. **Invest in planning**: Don't rush to the Work step. The plan document is where misunderstandings surface cheaply. Use plan mode or explicit planning prompts.
4. **Let the agent self-assess**: Before human review, have the agent review its own output and flag concerns. This catches issues before they consume human attention.
5. **Track the compounding**: Over time, the rules file grows. Each new rule prevents a class of future issues. The codebase becomes more AI-navigable with each PR.

**The 80/20 insight for PMs**: If your engineering team is spending 80% of time writing code and 20% on planning/review, they're not doing compound engineering — they're doing traditional engineering with AI typing. The compound engineering signature is the inverse: planning and evaluation dominate.

## Sources

### From: [2026-01-30 Compound Engineering: How Every Codes With Agents](../../sources/2026-01-30-compound-engineering-how-every-codes-with-agents.md)
**Key quote**: "In traditional engineering, you expect each feature to make the next feature harder to build—more complexity, more potential for bugs. In compound engineering, each feature makes the next one easier."
**Attribution**: Dan Shipper, Kieran Klaassen
**What this source adds**: The definitive framing of the compound engineering loop — names the four steps, establishes the 80/20 time distribution, and explains the mechanism (rules files as institutional memory). Grounded in Every's real-world operation of five products with minimal staffing.
**Links**: [Original](https://every.to/source-code/compound-engineering-how-every-codes-with-agents-af3a1bae-cf9b-458e-8048-c6b4ba860e62) | [Archive](../../sources/2026-01-30-compound-engineering-how-every-codes-with-agents.md)

## Related

- [Knowledge Capture as Side Effect](../horizontal/agents/system-design/instruction-design/knowledge-capture-as-side-effect.md) — The compound step IS knowledge capture as side effect, applied to engineering. The rules file grows as a byproduct of code review, not as a separate documentation task.
- [Plan Mode as Claude Code Default](../horizontal/agents/harnesses/plan-mode-as-claude-code-default.md) — The "Plan" step operationalized in Claude Code. Boris Cherny's 80% plan-mode workflow is compound engineering's Plan step in practice.
- [Intentional Understaffing for AI-First Teams](../ai-adoption/intentional-understaffing-ai-first-teams.md) — Every's single-person engineering teams are the organizational context that makes compound engineering necessary. The methodology and the org structure co-evolve.
- [Structured Context Loading](../horizontal/agents/system-design/instruction-design/structured-context-loading.md) — Rules files are one form of structured context that agents load at session start.
- [Spec-Driven Development](../adjacent-disciplines/spec-driven-development.md) — A related methodology shift. Where compound engineering keeps code but changes the process, spec-driven development eliminates code entirely for suitable components.
