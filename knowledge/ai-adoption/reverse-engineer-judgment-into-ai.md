---
created: 2026-02-07
updated: 2026-02-07
template: templates/knowledge-entry.md
template_version: 2
tags: [knowledge, ai-pm-craft, technique, custom-gpts, management]
status: draft
entry_type: technique
origin: sourced
featured: false
domain: professional-development
project: ai-pm-craft
---

# Reverse-Engineer Your Judgment into AI

## Summary

A technique for turning implicit expert judgment into an explicit, reusable AI evaluator. Instead of trying to articulate your quality standards from scratch (which is hard — you "know it when you see it"), you collect before/after examples and have AI analyze the patterns to discover your criteria. You then iteratively refine those criteria and encode them into a custom GPT that applies your standards consistently to new work.

The crucial move is starting open-ended — letting AI discover patterns without biasing it with your own framing — then getting "100 times more specific" to force it past vague principles into concrete, actionable standards.

## How to Apply

**When to use**: Whenever you repeatedly evaluate the same type of work (slide decks, PRDs, designs, code reviews, writing) and want to scale that evaluation to your team.

**Steps**:
1. **Collect examples**: Create a document with "before" (not great) and "after" (meets your standards) pairs. Save as PDF.
2. **Reverse-engineer with AI**: Upload to ChatGPT/Claude with an intentionally simple prompt — "Can you help me articulate the principles I am using?" Don't pre-bias the AI with your own framing.
3. **Refine iteratively**: Use the prompt "Be 100 times more specific" to force AI past platitudes. Add your own context about what matters most. Ask "What am I missing?"
4. **Build the evaluator**: Have AI write the GPT/agent instructions — "MY job is to create a GPT that can evaluate X... YOUR job is to write the prompt for it."
5. **Deploy to team**: Team members upload their work and get instant criteria-based feedback (ratings, specific suggestions, improvement paths).

**For AI PMs**: This technique is a microcosm of building any AI evaluation system. The before/after example collection is essentially creating an eval dataset. The iterative refinement is prompt engineering. The deployment is a lightweight AI product. Building one of these gives you firsthand experience with the full AI product lifecycle.

## Sources

### From: [[2026-02-07-hilary-gridley-scaling-yourself-custom-gpts]]
**Key quote**: "I kind of want the AI to start by interpreting this in ways that I might not even be able to predict. And then I'm gonna get an intune it and that's when I get super, super specific."
**Attribution**: Hilary Gridley
**What this source adds**: The complete "Deck Doctor" workflow from Hilary Gridley (Head of Core Product, WHOOP). Notable for the deliberate open-ended start — she avoids biasing the AI so it can discover patterns she might not have articulated herself. The "be 100x more specific" technique is a broadly applicable refinement step.
**Links**: [Original](https://www.chatprd.ai/how-i-ai/scaling-yourself-as-a-manager-with-custom-gpts) | [[2026-02-07-hilary-gridley-scaling-yourself-custom-gpts|Archive]]

## Related

- [[scale-manager-expertise-with-ai]]
- [[ai-as-writing-coach]]
