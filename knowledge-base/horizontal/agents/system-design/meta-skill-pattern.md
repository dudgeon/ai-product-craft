---
created: 2026-02-14
updated: 2026-02-14
template: templates/knowledge-entry.md
template_version: 4
tags: [knowledge, ai-pm, technique, agents, composability, skill-creation]
status: draft
entry_type: technique
origin: sourced
featured: false
domain: horizontal
horizontal_domain: agents
project: ai-pm
---

# Meta-Skill Pattern

## Summary

A technique for bootstrapping agent capabilities by building a "skill that builds skills" — a meta-skill that takes a description of a desired workflow and generates a properly structured skill folder (instruction file, templates, validation scripts). Instead of hand-authoring each new skill from scratch, you create one factory skill and then use it to produce domain-specific skills consistently and quickly.

The underlying insight is composability: agent skills aren't just endpoints — they can invoke and build on each other. A meta-skill is the simplest expression of this, but the pattern extends to any skill that orchestrates or generates other skills.

## How to Apply

**When to use**: When you need to create multiple skills and want consistency in structure, metadata, and quality. Especially useful when onboarding a team to skill-based workflows — the meta-skill encodes your conventions so each team member produces well-formed skills without memorizing the spec.

**When not to use**: For a single, one-off skill, the overhead of building a meta-skill isn't justified. Just create the skill directly.

**Steps**:
1. Create a `create_skill` (or similar) folder containing a `SKILL.md` that instructs the agent how to generate a new skill — including folder structure conventions, YAML metadata requirements, and template files to include
2. Optionally include a validation script (e.g., `validate_skill.py`) that checks YAML formatting, file references, and content structure. This bundles quality assurance into the generation process itself
3. Open your skills directory in an AI-native editor or start Claude Code in that directory — the agent auto-discovers the meta-skill from the filesystem
4. Prompt the agent: "Use the create_skill skill to create a skill for [your workflow]"
5. The agent reads the meta-skill instructions, generates the new skill folder, and (if validation is bundled) runs the validation script automatically
6. Review the generated skill, adjust the instruction file for tone/format, and iterate

**For AI PMs**: This pattern is relevant beyond personal productivity. It demonstrates how to scale agent capability creation across a team: instead of relying on one person to author all skills, you distribute a meta-skill that encodes your quality standards. The meta-skill becomes an onboarding tool — new team members can generate skills that meet your conventions from day one.

## Sources

### From: [2026-02-14 Claude Skills Explained Reusable AI Agents](../../../sources/2026-02-14-claude-skills-explained-reusable-ai-agents.md)
**Key quote**: "Instead of relying on Claude's built-in creator, I decided to build my own. I started a chat with Cursor's AI and gave it the official Anthropic Skills Documentation as context."
**Attribution**: Claire Vo
**What this source adds**: Vo demonstrates the full cycle: building a meta-skill in Cursor (~3 minutes), then using it via Claude Code to generate a changelog-to-newsletter skill. The meta-skill auto-generated a Python validation script alongside the instruction file — showing that skills can bundle executable tooling, not just natural language instructions. The article also surfaces a practical contrast: Claude's built-in skill creator over-generates (12 files when 5 suffice), while a hand-crafted meta-skill produces exactly what you specify.
**Links**: [Original](https://www.chatprd.ai/how-i-ai/claude-skills-explained) | [Archive](../../../sources/2026-02-14-claude-skills-explained-reusable-ai-agents.md)

## Related

- [Stepwise Task Execution](stepwise-task-execution.md) — another agent management technique from the same source ecosystem (ChatPRD)
