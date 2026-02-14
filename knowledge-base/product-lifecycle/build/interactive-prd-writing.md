---
created: 2026-02-07
updated: 2026-02-08
template: templates/knowledge-entry.md
template_version: 3
tags: [knowledge, ai-pm-craft, technique, prd, requirements]
status: draft
entry_type: technique
origin: sourced
featured: false
domain: product-lifecycle
lifecycle_phase: build
component: feature-specification-writing
project: ai-pm-craft
---

# Interactive PRD Writing with AI

## Summary

A technique for generating product requirements documents through AI-assisted conversation rather than writing them from scratch. The core mechanism has two parts: (1) **templatization** — a rule file that encodes what a good PRD looks like and how the AI should behave during generation, and (2) **structured follow-up questions** — the AI asks clarifying questions before writing, forcing the human to articulate context they'd otherwise skip.

The result is a complete PRD written at a level "suitable for a junior developer to understand" — a standard that forces explicitness, which is exactly what both AI agents and human collaborators need to execute without ambiguity. The PRD becomes a shared artifact that works as AI instruction *and* human communication document.

## How to Apply

**When to use**: Any feature or project where requirements aren't fully formed in your head yet, or where you need a written spec that others (human or AI) will execute against.

**When not to use**: Tasks so small they don't warrant a requirements doc. If you can describe it in 2-3 sentences, skip the PRD.

**Steps**:
1. Create a `generate_prd.md` rule file that defines: the AI's role, what a PRD is, what sections to include, and — critically — instructions to **ask clarifying questions before writing**
2. Key instruction in the rule file: write the PRD "suitable for a junior developer to understand." This forces the right level of explicitness
3. Invoke by @-including the rule file and providing a high-level feature description in one sentence
4. Answer the AI's follow-up questions honestly — this is where the real context-building happens
5. The AI generates a complete PRD covering functional requirements, non-goals, and technical considerations

**Why the follow-up questions matter**: Most people rush past context. The templatized rule file forces the AI to *pull* context out of you through questions, rather than relying on you to *push* it. This is a design pattern: make the right thing (thorough context) the default path, not the disciplined path.

**For AI PMs**: The PRD generated this way doubles as both an AI instruction document and a human-readable spec. This means the same artifact can brief an AI coding agent *and* align stakeholders. The "junior developer" framing is worth adopting broadly — it's a proxy for "explicit enough for an LLM to follow unambiguously."

## Sources

### From: [Ryan Carson's Structured AI Development](../../../sources/2026-02-07-ryan-carson-structured-ai-development.md)
**Key quote**: "The biggest mistake that I do, that everyone does is they try to rush through the context where you just don't have the patience to tell the AI what it actually needs to know to solve your problem."
**Attribution**: Ryan Carson
**What this source adds**: Carson's open-source `generate_prd.md` rule file provides the concrete implementation. The "junior developer" instruction is his key insight — it's a simple heuristic that produces AI-friendly documentation. The emphasis on the AI asking questions first (rather than immediately generating) is what makes this interactive rather than just templated.
**Links**: [Original](https://www.chatprd.ai/how-i-ai/ryan-carsons-3-step-playbook-for-structured-ai-development-in-cursor) | [Archive](../../../sources/2026-02-07-ryan-carson-structured-ai-development.md)

## Related

- [Task List Generation for Observability](task-list-generation-for-observability.md)
- [Stepwise Task Execution](../../horizontal/agents/stepwise-task-execution.md)
- [Context-First Development](context-first-development.md)
