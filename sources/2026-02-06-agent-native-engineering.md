---
created: 2026-02-06
updated: 2026-02-07
template: templates/source.md
template_version: 2
tags: [source, ai-pm-craft, agent-native, engineering-management]
status: unread
source_type: article
source_url: "https://www.generalintelligencecompany.com/writing/agent-native-engineering"
archive_url: "domains/professional-development/ai-pm-craft/sources/2026-02-06-agent-native-engineering.md"
author: "Andrew Pignanelli"
published: 2026-02-05
discovered: 2026-02-06
summary: "Orgs should restructure around agents as ICs, not just give engineers coding tools. Three task tiers: simple (one-shot), manageable (async agent + feedback), complex (sync). Kill two-engineer code review; combat slop with rulesets/tests/linters. $4k/eng/mo token spend yields 3-4x output. PMs/designers become the bottleneck as features ship at speed of thought."
domain: professional-development
project: ai-pm-craft
---

# Agent-Native Engineering

**By**: Andrew Pignanelli (Cofounder/CEO, The General Intelligence Company)
**Source**: [General Intelligence Company](https://www.generalintelligencecompany.com/writing/agent-native-engineering)
**Type**: article

## Summary

*Fill after reading. 2-3 sentences: what is this about, what's the core argument or insight?*

## Key Ideas Extracted

*Fill during processing. Each idea links to a knowledge entry.*

## Notes

*Your annotations, reactions, questions, disagreements. Written during or after reading.*

## Raw Content

Agent native engineering means restructuring your organization around agents as individual-contributors instead of engineers.

### Background: Background Agents Changed Everything

The shift started with Devin from Cognition AI (summer 2024) — first asynchronous coding agent. Assign a task, walk away, come back to new code in a PR. What mattered wasn't Devin's coding performance — it was the pattern of work it enabled: engineers operating two parallel work streams.

### Background Agents Engineering Workflow

1. Someone has a new feature idea scoped narrow enough
2. A Linear ticket is created
3. Ticket assigned to a person AND coding agent (someone still responsible)
4. Coding agent works in background, makes a PR
5. Agent iterates on CI/tests until they pass, checks for merge conflicts
6. Engineer reviews code, sometimes running branch locally
7. [Optional] Engineer leaves PR/ticket comments
8. Agent addresses feedback, makes new commits
9. Engineer approves and merges

### Three Task Levels

- **Simple (one-shottable):** Well-written prompt gets coded and merged easily. "Change the corner radius on this button."
- **Easily Manageable:** Background agent with some feedback cycles can solve.
- **Complex:** Managed directly by engineer using synchronous coding agents.

Every task except complex should be delegated. Agents become primary ICs, managed by engineers. Engineers become managers, managers become staff engineers.

### Agency Goes Up

Give engineers larger features with less specs. Give managers larger objectives. Stop requiring a second engineer to review every PR.

### Remove Two-Engineer Code Review

"A two engineer code review totally ruins this dynamic." If your engineer manages 5 simple, 2 manageable, 1 complex task — two-engineer review requires reviewing 10 simple, 4 manageable, 2 complex tasks. Alternatives: agentic pentesting companies, code review agents (Cursor Bugbot, Greptile), AI SRE on staging.

"In this new world you will live and die by the number of iterations you can complete in a given amount of time."

### Code Slop Prevention

- Robust rulesets (claude.md, .cursorrules) — "Agents are good at reading rules"
- Tests as reward signal — agent iterates until tests pass
- Linters (eslint, python black) for consistent styling
- Code review bots (Cursor Bugbot)

### How Agent-Native Engineering Affects an Org

- Engineers manage more, code less
- Task decomposition time also decreasing
- Ticketing system management becomes larger % of workflow
- "Everyone's a PM and team lead for whatever project they're working on"
- Products change rapidly; roadmaps >few weeks become ineffective
- Tight collaboration cycles, "actions-per-minute" mentality
- New problem: idea generation, not execution

### You Need More Designers and Product People

Engineer:designer ratio needs to change. "If your ratio was 1:20 like is fairly common at these orgs, it's now too low." Features materialize at speed of thought — need more people who can reason about experience, product, and design.

### Token Spend

$4,000/engineer/month on Opus tokens (January 2026). Engineers shipped average 20 PRs/day, sometimes hundreds of commits daily. "We are spending roughly 20% more on engineering intelligence to increase output by a factor of 3-4x."

### The Future

- IDEs as we know them will go away
- Code review by humans will go away
- All engineers become product managers, all PMs become engineers
- Highly capable background agent teams with everything delegated first
- Advanced plan mode UIs (akin to PRDs)
- Beautiful frontend code largely automated
- All infrastructure becomes code
- Teams become smaller and more capable
- Designers matter more, non-product-thinking engineers matter less
