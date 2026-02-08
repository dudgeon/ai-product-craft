---
created: 2026-02-07
updated: 2026-02-07
template: templates/knowledge-entry.md
template_version: 2
tags: [knowledge, ai-pm-craft, insight, context-engineering]
status: draft
entry_type: insight
origin: sourced
featured: false
domain: professional-development
project: ai-pm-craft
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

### From: [[2026-02-07-ryan-carson-structured-ai-development]]
**Key quote**: "The biggest mistake that I do, that everyone does is they try to rush through the context where you just don't have the patience to tell the AI what it actually needs to know to solve your problem."
**Attribution**: Ryan Carson
**What this source adds**: Carson frames context-building as the critical bottleneck in AI development and provides a concrete system (rule files + PRD + task decomposition) that forces you to slow down. The "junior developer" heuristic for PRD writing is a practical, memorable test.
**Links**: [Original](https://www.chatprd.ai/how-i-ai/ryan-carsons-3-step-playbook-for-structured-ai-development-in-cursor) | [[2026-02-07-ryan-carson-structured-ai-development|Archive]]

## Related

- [[interactive-prd-writing]]
- [[task-list-generation-for-observability]]
- [[stepwise-task-execution]]
- [[deliberate-context-selection]]
