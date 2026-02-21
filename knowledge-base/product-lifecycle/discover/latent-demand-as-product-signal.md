---
created: 2026-02-19
updated: 2026-02-19
template: templates/knowledge-entry.md
template_version: 5
tags: [knowledge, ai-pm]
status: draft
entry_type: technique
origin: sourced
featured: false
domain: product-lifecycle
lifecycle_phase: discover
component: problem-signal-detection
project: ai-pm
---

# Latent Demand as Product Signal

## Summary

Latent demand is the gap between what people *want* to do and what your product was designed to let them do. Users reveal this by hacking around constraints — using tools for purposes they weren't built for, building workarounds, or combining products in unexpected ways. This is high-signal product discovery: they've already proven the demand with their own effort, before you built anything.

The Claude Code → Cowork sequence is the canonical example. Cherny and team noticed users analyzing MRIs, recovering wedding photos from corrupted drives, and handling other distinctly non-coding tasks inside a coding tool. The latent demand for agentic AI assistance with complex knowledge work existed before anyone had thought to name it. Cowork emerged from making that latent behavior easier, not from imagining a new use case.

## How to Apply

1. **Instrument for off-label behavior.** Look at how users actually use your product — support tickets, session recordings, usage patterns at the edges — not just the happy path you designed.
2. **Treat workarounds as demand signals.** If users are doing something awkward or difficult that your product wasn't designed for, ask: what would it take to make that native?
3. **Resist the urge to correct it.** The instinct is often to say "that's not what this is for." Instead, ask: why are they doing this? What does it tell us about unmet demand?
4. **Build for the demand that already exists, not the demand you imagine.** Latent demand reduces the risk of discovery bets because users have already demonstrated it with their own behavior.

This is distinct from user interviews or surveys, which ask users to articulate needs they may not have language for. Latent demand surfaces itself through behavior.

## Sources

### From: [2026-02-19 Head of Claude Code: What Happens After Coding Is Solved](../../sources/2026-02-19-head-of-claude-code-boris-cherny.md)
**Key quote**: "Look for 'latent demand.' Claude Code was built by observing what people were already trying to do, and then making it easier. Cowork emerged when they noticed people using Claude Code for non-coding tasks like analyzing MRIs or recovering wedding photos from corrupted drives."
**Attribution**: Boris Cherny
**What this source adds**: Concrete example of latent demand → product: Claude Code's observed off-label use (MRI analysis, photo recovery) preceded the Cowork product by months. The demand signal predated any deliberate discovery effort.
**Links**: [Original](https://www.lennysnewsletter.com/p/head-of-claude-code-what-happens) | [Archive](../../sources/2026-02-19-head-of-claude-code-boris-cherny.md)

## Related

- [Decision-Anchored Analysis Context](decision-anchored-analysis-context.md) — Once demand is identified, anchor analysis to the specific decision the demand surfaces
- [Parallel Prototyping for Clarity](../shape/parallel-prototyping-for-clarity.md) — After identifying latent demand, parallel prototyping is a fast way to explore solution space
