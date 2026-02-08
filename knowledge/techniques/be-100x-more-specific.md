---
created: 2026-02-07
updated: 2026-02-07
template: templates/knowledge-entry.md
template_version: 2
tags: [knowledge, ai-pm-craft, technique, prompting, refinement]
status: draft
entry_type: technique
origin: sourced
featured: false
domain: professional-development
project: ai-pm-craft
---

# "Be 100x More Specific"

## Summary

A prompting technique for forcing AI past vague, platitude-level outputs into concrete, actionable specifics. When AI generates a first-draft list of principles, criteria, or guidelines, the prompt "Be 100 times more specific" pushes it to a qualitatively different level of detail — from "use clear headlines" to specifiable, evaluable standards with examples.

The technique works because LLMs tend to produce safe, generic outputs on the first pass. The specificity demand acts as a constraint that forces the model to commit to concrete standards rather than hedging with generalities. It's broadly applicable beyond any single use case — works for evaluation criteria, writing standards, code review guidelines, process documentation, and anywhere you need actionable precision.

## How to Apply

**When to use**: Whenever AI output is correct but vague. Particularly effective after AI has done an initial analysis (e.g., reverse-engineering criteria from examples, summarizing best practices, generating rubrics).

**When not to use**: When the initial output is already concrete and specific, or when you need creative/divergent thinking rather than precision.

**The pattern**:
1. Get a first-draft output from AI (list of principles, criteria, guidelines)
2. Prompt: "Be 100 times more specific"
3. AI rewrites with concrete, measurable, actionable standards
4. Blend AI specifics with your own expert judgment — add what matters most, remove what doesn't apply
5. Optionally ask "What am I missing?" to cover blind spots

**Why "100 times" works**: The exaggeration is the point. "Be more specific" gets you 20% better. "Be 100 times more specific" signals that you want a qualitatively different level of output — not a refinement, but a transformation from category to instance.

**For AI PMs**: This technique is directly useful in prompt engineering, eval design, and writing product specs. Anywhere you need to turn qualitative standards ("good UX") into measurable criteria ("task completion rate above 90% in under 3 clicks"), this prompt pattern gets you there faster.

## Sources

### From: [[2026-02-07-hilary-gridley-scaling-yourself-custom-gpts]]
**Key quote**: "I kind of want the AI to start by interpreting this in ways that I might not even be able to predict. And then I'm gonna get an intune it and that's when I get super, super specific."
**Attribution**: Hilary Gridley
**What this source adds**: Gridley uses this in the context of building a "Deck Doctor" GPT — after AI reverse-engineers her implicit slide evaluation criteria from before/after examples, "be 100x more specific" is the refinement step that makes those criteria actionable enough to power a custom evaluator. She notes this technique is "broadly applicable beyond slide evaluation."
**Links**: [Original](https://www.chatprd.ai/how-i-ai/scaling-yourself-as-a-manager-with-custom-gpts) | [[2026-02-07-hilary-gridley-scaling-yourself-custom-gpts|Archive]]

## Related

- [[reverse-engineer-judgment-into-ai]]
- [[context-first-development]]
