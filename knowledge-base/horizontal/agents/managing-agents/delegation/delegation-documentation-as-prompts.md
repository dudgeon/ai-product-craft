---
created: 2026-02-16
updated: 2026-02-16
template: templates/knowledge-entry.md
template_version: 4
tags: [knowledge, ai-pm, insight, agents, managing-agents, delegation, documentation, prompting]
status: draft
entry_type: insight
origin: sourced
featured: false
domain: horizontal
horizontal_domain: agents
lifecycle_phase: build
project: ai-pm
---

# Delegation Documentation as Agent Prompts

## Summary

Every field has independently invented structured documentation for delegating work: PRDs (product management), shot lists (film), Five Paragraph Orders (military), engagement scopes (consulting), design intent documents (architecture). These all solve the same fundamental problem — getting what's in one person's head into another person's actions — and they all work remarkably well as AI prompts for the same reason.

The insight is that effective AI delegation isn't a new skill requiring new formats. The documentation practices that fields have refined over decades for human-to-human delegation translate directly to human-to-agent delegation. They share common structural elements that make them effective for both audiences.

## How to Apply

**When to use**: When crafting delegation instructions for AI agents on complex tasks. Rather than inventing prompting formats from scratch, adapt the delegation documentation format your field already uses. If your field doesn't have one, borrow from one that does.

**When not to use**: For simple, one-shot requests where a brief instruction suffices. The overhead of full delegation documentation isn't warranted for tasks that take less than the time to write the document.

**Common elements across delegation formats**:
1. **What are we trying to accomplish and why?** — Purpose and context
2. **Where are the limits?** — Authority boundaries, scope constraints
3. **What does "done" look like?** — Success criteria, acceptance conditions
4. **What outputs do I need?** — Specific deliverables
5. **What interim outputs demonstrate progress?** — Checkpoints, milestones
6. **What quality checks happen before completion?** — Verification criteria

**Application by field**:
- **Product management** → PRDs with requirements, acceptance criteria, success metrics
- **Military** → Five Paragraph Orders: situation, mission, execution, sustainment, command
- **Film** → Shot lists: what's in frame, camera movement, lighting, mood
- **Consulting** → Engagement scopes: objectives, deliverables, timeline, assumptions
- **Engineering** → Technical design documents: problem, approach, constraints, alternatives considered

**For AI PMs**: This insight has two implications. First, for your *own* agent management: use your existing PRD-writing skills as-is for complex agent delegation. Second, for *product design*: if you're building agent-powered products, consider incorporating your users' existing delegation documentation formats as input templates rather than inventing new prompt formats. Users already know how to write these — leverage that fluency.

**Connection to prompting**: This sits above the prompting horizontal domain. Individual prompting techniques (be 100x more specific, my-job-your-job delineation) are components that live *within* these delegation documents. The document is the container; prompting patterns are the ingredients.

## Sources

### From: [2026-01-27 Management as AI Superpower](../../../sources/2026-01-27-ethan-mollick-management-as-ai-superpower.md)
**Key quote**: "All of these are really the same thing: attempts to get what's in one person's head into someone else's actions."
**Attribution**: Ethan Mollick
**What this source adds**: The cross-field inventory of delegation documentation formats and the insight that they're all structurally the same. The six common elements (purpose, limits, done-state, outputs, checkpoints, quality) provide a portable checklist for delegation in any context. The most novel contribution is the reframing: prompting isn't a new AI skill, it's delegation — and we've been practicing delegation for decades.
**Links**: [Original](https://www.oneusefulthing.org/p/management-as-ai-superpower) | [Archive](../../../sources/2026-01-27-ethan-mollick-management-as-ai-superpower.md)

## Related

- [Delegation Decision Framework](../task-fit/delegation-decision-framework.md) — once you've decided to delegate, this entry covers what effective delegation documentation looks like
- [Talent-to-Direction Scarcity Shift](../talent-to-direction-scarcity-shift.md) — why delegation skill matters: knowing what to ask for is the scarce resource
- [Interactive PRD Writing](../../../../product-lifecycle/build/interactive-prd-writing.md) — a specific implementation of delegation documentation for the build phase, using AI to co-create the PRD itself
- [Be 100x More Specific](../../../prompting/be-100x-more-specific.md) — a prompting-layer technique that lives *inside* delegation documents
- [My Job Your Job Role Delineation](../../../prompting/my-job-your-job-role-delineation.md) — another prompting-layer technique applicable within delegation documentation
