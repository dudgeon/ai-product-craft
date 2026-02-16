---
created: 2026-02-07
updated: 2026-02-14
template: templates/knowledge-entry.md
template_version: 3
tags: [knowledge, ai-pm, insight, context-engineering]
status: draft
entry_type: insight
origin: sourced
featured: false
domain: product-lifecycle
lifecycle_phase: build
project: ai-pm
---

# Context-First Development

## Summary

The single most common failure mode in AI-assisted development is rushing past context. Developers (and PMs) jump straight to asking the AI to build something without first establishing what it needs to know. The counterintuitive principle: slowing down to provide thorough context — writing a PRD, defining requirements, explaining constraints — actually speeds everything up because the AI produces correct output on the first pass instead of requiring multiple correction cycles.

A practical heuristic: write as if you're instructing a "junior developer." This level of explicitness is exactly what LLMs need to avoid ambiguity, and it also produces better documentation for humans.

## How to Apply

**When to use**: Always. This is a default posture, not a specific technique.

**Concrete practices**:
- Before asking AI to build anything, write down what "done" looks like
- Use the "junior developer" test: would a smart but inexperienced person know exactly what to build from your instructions?
- When AI output is wrong, your first question should be "what context was it missing?" not "is the model bad?"
- Invest in reusable context artifacts (rule files, CLAUDE.md, PRD templates) that compound over time

**For AI PMs**: This insight maps directly to prompt engineering and eval design. If your AI feature is underperforming, the problem is more often context than capability. This is also the foundation of "context engineering" as a discipline.

## Sources

### From: [Ryan Carson's Structured AI Development](../../../sources/2026-02-07-ryan-carson-structured-ai-development.md)
**Key quote**: "The biggest mistake that I do, that everyone does is they try to rush through the context where you just don't have the patience to tell the AI what it actually needs to know to solve your problem."
**Attribution**: Ryan Carson
**What this source adds**: Carson frames context-building as the critical bottleneck in AI development and provides a concrete system (rule files + PRD + task decomposition) that forces you to slow down. The "junior developer" heuristic for PRD writing is a practical, memorable test.
**Links**: [Original](https://www.chatprd.ai/how-i-ai/ryan-carsons-3-step-playbook-for-structured-ai-development-in-cursor) | [Archive](../../../sources/2026-02-07-ryan-carson-structured-ai-development.md)

### From: [2026-02-08 Getting Paid to Vibe Code](../../../sources/2026-02-08-vibe-coding-new-ai-job.md)
**Key quote**: "The ceiling on AI output isn't model intelligence — it's what the model is told and shown before it acts."
**Attribution**: Lazar Jovanovic (via Lenny Rachitsky)
**What this source adds**: Quantifies the principle as an 80/20 split — Jovanovic spends 80% of his time planning and chatting with AI agents and only 20% building. This is a practitioner-validated ratio from someone shipping production products (Shopify integrations, internal dashboards) purely through AI tools. Where Carson frames context-first as avoiding a mistake, Jovanovic frames it as a deliberate time allocation strategy.
**Links**: [Original](https://www.lennysnewsletter.com/p/getting-paid-to-vibe-code) | [Archive](../../../sources/2026-02-08-vibe-coding-new-ai-job.md)

## Related

- [Interactive PRD Writing](interactive-prd-writing.md)
- [Task List Generation for Observability](task-list-generation-for-observability.md)
- [Stepwise Task Execution](../../horizontal/agents/skills/stepwise-task-execution.md)
- [Deliberate Context Selection](../../horizontal/context/deliberate-context-selection.md)
- [Structured Context Loading](../../horizontal/agents/skills/structured-context-loading.md) — The systematic implementation of context-first: purpose-built files loaded before each interaction
- [Parallel Prototyping for Clarity](../../product-lifecycle/shape/parallel-prototyping-for-clarity.md) — A way to build context through exploration rather than upfront specification
