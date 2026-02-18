---
created: 2026-02-14
updated: 2026-02-14
template: templates/knowledge-entry.md
template_version: 4
tags: [knowledge, ai-pm, technique, agents, self-reflection, behavioral-analysis]
status: draft
entry_type: technique
origin: sourced
featured: false
domain: horizontal
horizontal_domain: agents
project: ai-pm
---

# Agent-Mediated Self-Reflection

## Summary

Using an AI agent not to *do* work but to *observe* your work patterns and surface insights you can't see yourself. The agent ingests your digital exhaust — meeting recordings, journal entries, git commits, Slack conversations — and looks for patterns: behavioral tendencies, intention-action gaps, recurring learnings you didn't consciously capture.

This is qualitatively different from asking an AI "give me feedback on this document." The agent isn't evaluating a deliverable; it's analyzing your *behavior over time*. Dan Shipper feeds it meeting recordings and asks it to identify moments of conflict avoidance. Gang Rui runs a weekly analysis of journal entries + git commits to spot gaps between what he said he'd do and what he actually did. Chad Boyda reviews Slack conversations to find moments where he learned something but didn't consciously register it.

The pattern works because humans are poor observers of their own behavioral tendencies. We rationalize, forget, and selectively remember. An agent processing raw behavioral data (transcripts, commits, chats) can identify patterns across weeks of activity that no single moment of introspection would catch.

## How to Apply

**When to use**: When you want to improve behavioral patterns — leadership habits, time allocation, follow-through on intentions, learning capture — and have digital artifacts of your behavior.

**Pattern**:
1. **Accumulate behavioral data**: Meeting recordings (Granola, Fireflies), journal entries, git commits, Slack logs, calendar data. The richer and more honest the data, the better the analysis.
2. **Define what to look for**: Don't just say "analyze this." Specify the behavioral dimension: conflict avoidance, follow-through gaps, communication patterns, decision-making biases.
3. **Run periodically**: Gang Rui's weekly cadence (slash command that runs on 7 days of data) is a good starting point. Too frequent → noise. Too infrequent → patterns fade.
4. **Act on findings**: The agent's output should feed into a system improvement loop, not just self-awareness. Gang Rui's agent doesn't just identify gaps — it suggests system improvements.

**What makes each example powerful**:
- Dan Shipper: *conflict avoidance in meetings* — something a coach would notice but you'd rationalize away
- Gang Rui: *intention-action gap* — journal says "I will X" but git shows you did Y. The commit history is the ground truth.
- Chad Boyda: *unregistered learning* — you solved a problem in Slack but didn't capture the lesson. The agent finds these moments.

**For AI PMs**: This technique suggests a product category: "AI behavioral coach." The agent isn't a productivity tool — it's a mirror with memory. Product opportunities exist for leadership development, team dynamics analysis, and habit formation.

## Sources

### From: [2026-02-13 Everyone Should Use Claude Code More](../../../../sources/2026-02-13-everyone-should-use-claude-code-more.md)
**Key quote**: "I download all of my meeting recordings, put them in a folder, and ask Claude Code to tell me all of the times I've subtly avoided conflict."
**Attribution**: Dan Shipper
**What this source adds**: Three independent examples of the self-reflection pattern from different users, each targeting a different behavioral dimension (conflict avoidance, intention-action gaps, unregistered learning). Gang Rui's implementation as a slash command with system-improvement output is the most developed version — it closes the loop from observation to action.
**Links**: [Original](https://www.lennysnewsletter.com/p/everyone-should-be-using-claude-code) | [Archive](../../../../sources/2026-02-13-everyone-should-use-claude-code-more.md)

## Related

- [Knowledge Capture as Side Effect](../instruction-design/knowledge-capture-as-side-effect.md) — Chad Boyda's pattern (identifying learnings from Slack) is a form of knowledge capture; the self-reflection agent surfaces what should be persisted
- [Agent as Cross-Tool Workflow Hub](../architecture/agent-as-cross-tool-workflow-hub.md) — the self-reflection agent needs access to multiple data sources (meetings, journals, commits), making it a specialized cross-tool pattern
- [Tool Identity as Adoption Gate](../../../../ai-adoption/tool-identity-as-adoption-gate.md) — from the same source; self-reflection is one of the non-obvious use cases hidden behind the "Code" branding
