---
created: 2026-02-19
updated: 2026-02-19
template: templates/knowledge-entry.md
template_version: 5
tags: [knowledge, ai-pm]
status: draft
entry_type: insight
origin: sourced
featured: false
domain: ai-adoption
project: ai-pm
---

# Delay Token Cost Optimization

## Summary

The instinct to optimize AI token costs early kills experimentation. During the exploratory phase of any AI project, token cost is not the real cost — engineer time is. An engineer's hourly cost typically dwarfs the token cost of any experiment they might run. Constraining tokens to save money at this stage is the wrong tradeoff: you're trading a cheap input (tokens) for a scarce one (ideas, velocity, discovery).

Boris Cherny's principle at Anthropic: give teams unlimited tokens during experimentation. Don't optimize cost until an idea has proven it scales. At scale, token cost becomes meaningful and optimization is warranted — but at small scale, the cost calculus almost always favors experimentation. A team that's worried about token spend will unconsciously constrain its exploration.

## How to Apply

- **For new AI projects or teams exploring AI-native workflows**: Remove token budgets entirely during the first phase. Set a review trigger (e.g., "when cost exceeds $X/day" or "when the approach is validated") to revisit.
- **For individual practitioners**: Don't shortcut by using cheaper models or shorter prompts during exploration. Full-capability, full-context runs during learning phases produce better results and better intuitions.
- **Reframe the cost question**: The relevant question isn't "how much are we spending on tokens?" — it's "are we discovering things that would be worth scaling?" If yes, the token cost is negligible. If no, the problem isn't the tokens.
- **When to start optimizing**: After an approach proves it scales. That might mean model downgrade (Opus → Sonnet → Haiku), prompt compression, caching, or batching. All of these make sense *after* you've validated the approach.

The asymmetry: the cost of premature optimization is discovery you never did. The cost of delayed optimization is tokens on something that already works. The latter is a much better problem to have.

## Sources

### From: [2026-02-19 Head of Claude Code: What Happens After Coding Is Solved](../sources/2026-02-19-head-of-claude-code-boris-cherny.md)
**Key quote**: "At small scale, the token cost is still relatively low compared to their salary. If an idea works and scales, that's when you optimize it."
**Attribution**: Boris Cherny
**What this source adds**: Grounded in Anthropic's actual practice — the people who build Claude Code and have the most visibility into token economics are deliberately *not* optimizing token cost during experimentation. The principle comes from the source most incentivized to conserve tokens.
**Links**: [Original](https://www.lennysnewsletter.com/p/head-of-claude-code-what-happens) | [Archive](../sources/2026-02-19-head-of-claude-code-boris-cherny.md)

## Related

- [Intentional Understaffing for AI-First Teams](intentional-understaffing-ai-first-teams.md) — Pairing both creates the right AI-first environment: constrain headcount, not tokens
- [Capability Over Cost in Model Selection](../horizontal/agents/managing-agents/selection/capability-over-cost-in-model-selection.md) — Related: the cheapest model isn't the right default; capability matters more than cost at the point of use
