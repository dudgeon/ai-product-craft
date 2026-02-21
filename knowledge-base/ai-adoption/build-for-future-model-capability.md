---
created: 2026-02-19
updated: 2026-02-19
template: templates/knowledge-entry.md
template_version: 5
tags: [knowledge, ai-pm]
status: draft
entry_type: mental-model
origin: sourced
featured: false
domain: ai-adoption
project: ai-pm
---

# Build for Future Model Capability

## Summary

When building AI-native products, optimize for the model capabilities that will exist in six months — not the ones that exist today. The implication: accept poor product-market fit early as the cost of being ready when that model ships. This inverts standard product intuition, which says to find PMF as fast as possible. In fast-moving AI, the product that fits today's model may be obsolete when the next model arrives; the product that's slightly ahead of today's capabilities will hit the ground running.

Boris Cherny runs this principle explicitly at Claude Code: design decisions are made with the assumption of capabilities that aren't quite available yet. When those capabilities land, the product is already positioned to leverage them fully. The alternative — optimizing for current model performance — means constant catch-up as models improve.

## How to Apply

- **At product design time**: Ask "if the model were twice as capable six months from now, what would this feature look like? Design for that, not for what the model can do today."
- **For investor/stakeholder communication**: Frame early PMF struggles as intentional positioning, not product failure. "We're building for the model that ships in Q3" is a different narrative than "we're struggling to find fit."
- **For roadmap prioritization**: Deprioritize work that optimizes around current model limitations (workarounds, fallbacks). Prioritize work that unlocks value when limitations are removed.
- **For team calibration**: Set a 6-month "target model" assumption and use it as a shared design constraint across the team. Avoids building for the wrong horizon.

The discomfort to accept: your product will feel ahead of its time early. That's the point. The timing risk is real — "six months out" requires judgment — but the alternative (designing for today) guarantees you're always one model release behind.

## Sources

### From: [2026-02-19 Head of Claude Code: What Happens After Coding Is Solved](../sources/2026-02-19-head-of-claude-code-boris-cherny.md)
**Key quote**: "It's going to be uncomfortable because your product-market fit won't be very good for the first six months. But when that model comes out, you'll hit the ground running."
**Attribution**: Boris Cherny
**What this source adds**: First-person validation from the creator of one of the fastest-growing AI developer tools. Cherny runs this principle explicitly at Claude Code — it's not a theoretical suggestion.
**Links**: [Original](https://www.lennysnewsletter.com/p/head-of-claude-code-what-happens) | [Archive](../sources/2026-02-19-head-of-claude-code-boris-cherny.md)

## Related

- [Intentional Understaffing for AI-First Teams](intentional-understaffing-ai-first-teams.md) — Complementary: understaffing forces AI adoption now; future-model design frames *what* you're building toward
- [AI Disrupts Strategic PM Skills Most](ai-disrupts-strategic-pm-skills-most.md) — The strategic PM skills that matter most are exactly those needed to anticipate where AI capabilities are heading
