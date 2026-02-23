---
created: 2026-02-17
updated: 2026-02-23
template: templates/source.md
template_version: 3
tags: [source, ai-pm]
status: processed
source_type: article
source_url: "https://every.to/source-code/compound-engineering-how-every-codes-with-agents-af3a1bae-cf9b-458e-8048-c6b4ba860e62"
archive_url: "domains/professional-development/ai-pm/sources/2026-01-30-compound-engineering-how-every-codes-with-agents.md"
author: "Dan Shipper, Kieran Klaassen"
published: 2026-01-30
discovered: 2026-02-17
summary: "Dan Shipper and Kieran Klaassen describe Every's 4-step compound engineering loop: Plan (agent researches and writes implementation plan), Work (agent writes code and tests), Assess (agent and human review output), Compound (learnings get encoded into rules/skills that make the next loop smarter). 80% of engineering time is now in planning and review, not writing code. Key insight: bugs and performance issues become permanent institutional memory via automated rules, not just one-time fixes."
domain: professional-development
project: ai-pm
scraped_by: claude
---

# Compound Engineering: How Every Codes With Agents

**By**: Dan Shipper, Kieran Klaassen
**Source**: [Original URL](https://every.to/source-code/compound-engineering-how-every-codes-with-agents-af3a1bae-cf9b-458e-8048-c6b4ba860e62)
**Type**: article

## Summary

Dan Shipper and Kieran Klaassen define "compound engineering" — the methodology Every uses to run five software products with minimal staffing. Core insight: when agents write 100% of code, complexity debt inverts — each feature makes the next *easier* through encoded learnings. The four-step loop (Plan, Work, Assess, Compound) shifts 80% of engineering time to planning and review. The "compound" step — encoding bugs, design decisions, and code review lessons into rules files — is what makes the loop self-improving.

## Key Ideas Extracted

- [Compound Engineering Loop](../knowledge-base/software-methodology/compound-engineering-loop.md) — The core four-step methodology (Plan → Work → Assess → Compound) as a mental model for agent-first software development
- [Knowledge Capture as Side Effect](../knowledge-base/horizontal/agents/system-design/instruction-design/knowledge-capture-as-side-effect.md) — (enriched) The compound step is this pattern applied to engineering: rules files grow as a byproduct of code review
- [Intentional Understaffing for AI-First Teams](../knowledge-base/ai-adoption/intentional-understaffing-ai-first-teams.md) — (enriched) Five products, each run by one or two people, as the enabling organizational context

## Notes

- The article is relatively brief — it describes the loop at a high level. The companion sources (Definitive Guide, individual step articles) likely go deeper into each step.
- "Source Code" column version of the article originally published in "Chain of Thought" column on 2025-12-11. Same URL slug with different column prefix.
- Related sources for deeper treatment: `2026-01-28-stop-coding-and-start-planning.md` (Plan step), `2026-01-29-teach-your-ai-to-think-like-senior-engineer.md` (planning strategies), `2026-02-09-compound-engineering-definitive-guide.md` (comprehensive guide), `2026-compound-engineering-guide.md` (full guide).
- Duplicate source exists at `2026-02-12-compound-engineering-every-codes-agents-v2.md` (same URL, bulk-added without content).

## Raw Content

**Compound Engineering: How Every Codes With Agents**
*A four-step engineering process for software teams that don't write code*

By Dan Shipper and Kieran Klaassen | January 30, 2026 | Source Code

What happens to software engineering when 100 percent of your code is written by agents? This is a question we've had to wrestle with as AI coding has become so powerful that our team rarely writes code by hand anymore.

So much of engineering until now assumed that coding is hard and engineers are scarce. Removing those constraints opens up an entirely new style of engineering we call compound engineering.

In traditional engineering, you expect each feature to make the next feature harder to build—more complexity, more potential for bugs. In compound engineering, each feature makes the next one easier. That was a real a-ha moment for us.

We run five software products in-house (and are incubating a few more), each of which is run mostly by one or two people. This shift has huge implications for how software is built at every company.

**Compound engineering loop**

A compound engineer orchestrates agents running in parallel, who plan, write, and evaluate code. The loop has four steps:

- **Plan:** Agents read issues, research approaches, and synthesize information into detailed implementation plans.
- **Work:** Agents write code and create tests according to those plans.
- **Review:** The engineer reviews the output itself and the lessons learned from the output.
- **Compound:** The engineer feeds the results back into the system, where they make the next loop better by helping the agent write better code.

We use Anthropic's Claude Code primarily for compound engineering, but it is tool-agnostic—some members of our team use Droid, Codex CLI, and our own compound engineering plugin.

Roughly 80 percent of compound engineering is in the plan and review parts, while 20 percent is in the work and compound parts.

**1. Plan**

In a world where agents are writing all of your code, planning is where most of a developer's time is spent. Before starting any task, the agent reads the codebase and even its commit history. Once the research is complete, the agent writes a plan—usually a text document that lives either in the codebase itself or in a GitHub issue.

Planning helps build a shared mental model between you and the agent for exactly what you're building and how to build it. As models get better, especially with small projects, you have to plan less and less—the agent just figures it out.

**2. Work**

The easiest step: you tell the agent to start working. The agent reads the plan, implements it, and creates tests. One of the most important tricks is using a model context protocol like Playwright or Claude Code's headless browser to let the agent test its own work directly in the browser.

**3. Assess**

In the assessment step, we ask the agent to review its own work, and we review the work too. This can include automated tools like linters and unit tests. The compound engineering plugin, for example, asks Claude to describe the "lessons learned" from each code review.

**4. Compound**

This is the money step. We take what we learned in any of the previous steps—bugs, potential performance issues, edge cases—and encode them as rules in our codebase that the agent reads at the beginning of each new task.

For example, in the Cora codebase, before building anything new, the agent reads a comprehensive set of rules built up from every bug fix, design decision, and code review we've ever done. These rules are built up in a mostly automated fashion—after a code review, we'll ask Claude to summarize what we learned and add that to the rules file.

The beauty of this is that learnings are automatically distributed to the team. Because the rules live in the codebase, every team member—and every agent—reads them.
