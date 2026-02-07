---
created: 2026-02-07
updated: 2026-02-07
template: templates/knowledge-entry.md
template_version: 1
tags: [knowledge, ai-pm-craft, technique, prompting, role-delineation]
status: draft
entry_type: technique
domain: professional-development
project: ai-pm-craft
---

# "My Job / Your Job" Role Delineation

## Summary

A prompting technique that explicitly partitions responsibility between the human and the AI by stating "MY job is X. YOUR job is Y." This creates a clear contract that prevents two common failure modes: the AI overstepping (trying to do your thinking for you) and the AI understepping (producing vague output because it doesn't know what's expected).

The technique works because it gives the AI a precise scope and a clear deliverable. Instead of a fuzzy request ("help me build a GPT"), the AI receives a bounded task with defined inputs (your criteria, your context) and a defined output format (a complete set of GPT instructions). The human retains ownership of the *what* and *why* while delegating the *how* of a specific artifact.

## How to Apply

**When to use**: Whenever you need the AI to produce a specific artifact (instructions, a template, a plan, a rubric) and you want to retain ownership of the strategic decisions that inform it.

**The pattern**:
```
MY job is [what you own — the context, criteria, judgment, decisions].
YOUR job is [what you want the AI to produce — a specific, bounded deliverable].
```

**Examples**:
- "MY job is to create a GPT that evaluates slide decks based on my specific criteria. YOUR job is to write the prompt for it."
- "MY job is to define what good code review looks like on this team. YOUR job is to turn that into a checklist an AI reviewer can follow."
- "MY job is to decide what this product should do. YOUR job is to write the PRD that captures those decisions."

**Why this works beyond simple task assignment**: The "my job / your job" framing does three things simultaneously:
1. **Scopes the AI's authority** — it knows what decisions it can make and which ones belong to you
2. **Sets the output format** — "write the prompt" is more specific than "help me build a GPT"
3. **Preserves human agency** — by explicitly claiming ownership of the judgment, you prevent the AI from substituting its own values or criteria

**For AI PMs**: This pattern maps directly to how AI features should delineate user vs. system responsibility. When designing an AI-assisted workflow, the question "what's the user's job and what's the AI's job?" is the fundamental UX decision. This prompting technique is a microcosm of that design problem.

## Sources

### From: [[2026-02-07-hilary-gridley-scaling-yourself-custom-gpts]]
**Key quote**: "My job is to create a GPT that can evaluate slide decks for people on my team based on my specific criteria that I care about. It's really important to me that this GPT explains the criteria, why it matters, and gives the user specific feedback on how to improve. YOUR job is to write the prompt for it."
**What this source adds**: Gridley uses this in the context of building a custom GPT evaluator — she retains ownership of the quality standards and delegates the prompt engineering to the AI. The result is a detailed set of GPT instructions including persona, evaluation criteria, and feedback format. Notable that she embeds her requirements *within* the role delineation itself ("it's really important to me that..."), making the handoff information-rich rather than just structural.
**Links**: [Original](https://www.chatprd.ai/how-i-ai/scaling-yourself-as-a-manager-with-custom-gpts) | [[2026-02-07-hilary-gridley-scaling-yourself-custom-gpts|Archive]]

## Related

- [[be-100x-more-specific]]
- [[reverse-engineer-judgment-into-ai]]
- [[interactive-prd-writing]]
