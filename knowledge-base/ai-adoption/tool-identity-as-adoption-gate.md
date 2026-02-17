---
created: 2026-02-14
updated: 2026-02-14
template: templates/knowledge-entry.md
template_version: 4
tags: [knowledge, ai-pm, insight, adoption, positioning, naming]
status: draft
entry_type: insight
origin: sourced
featured: false
domain: ai-adoption
project: ai-pm
---

# Tool Identity as Adoption Gate

## Summary

When an AI tool has broad capability but narrow adoption, the bottleneck may be the tool's *identity* — its name, branding, and implied audience — not its capability. Claude Code serves 50+ non-technical use cases (lead gen, invoice management, self-reflection, cross-tool workflows, writing, research), yet adoption was gated by the word "Code," which signals "for developers" and prevents non-technical users from even trying it.

Lenny's reframe is the proof: "forget that it's called Claude Code and instead think of it as Claude Local or Claude Agent." Helen Lee Kupp, a non-developer mom using voice notes on stroller walks, captures the barrier precisely: "The terminal interface? Overwhelming at first. The word 'Code'... but what if I don't have a 'coding project'?" She tried it anyway and found it transformed her entire workflow.

The generalizable pattern: if your AI product isn't reaching the users it could serve, audit the tool's identity before auditing its features. Naming, positioning, and first-run experience all create implicit filters on who self-selects in.

## How to Apply

**When to use**: When launching or evaluating adoption of an AI tool/feature and noticing that a capable tool has a narrower user base than expected.

**The diagnostic**:
1. Who *could* this tool serve? (capability audit)
2. Who *does* this tool serve? (adoption reality)
3. If there's a gap, what signals are filtering people out? (identity/positioning/onboarding)

**Key levers**:
- **Naming**: Does the tool's name constrain who tries it? "Code" → developers. "Agent" → technical users. "Assistant" → everyone.
- **First-run experience**: Does setup require technical confidence (terminal, CLI) even if daily use doesn't? Lenny recommends Warp to smooth the terminal onboarding.
- **Use case framing**: Are you marketing capability ("local AI agent with filesystem access") or outcomes ("organize your life, automate your busywork")?
- **The "local" nuance**: Lenny's footnote reveals that "local" is itself a framing choice — "Claude Code does not actually run 'locally' on your machine—the AI/LLM processing happens in the cloud—but you run the commands locally, it has access to all your local files, and it's specifically designed to feel 'local.'" The perception of locality matters as much as the reality.

**For AI PMs**: When scoping AI features for broad adoption, pressure-test whether the tool's identity matches the intended audience. Run the "50 use cases" exercise — brainstorm non-obvious use cases outside your primary persona. If the list is long, your adoption gap is probably positioning, not capability.

## Sources

### From: [2026-02-13 Everyone Should Use Claude Code More](../../sources/2026-02-13-everyone-should-use-claude-code-more.md)
**Key quote**: "The key is to forget that it's called Claude Code and instead think of it as Claude Local or Claude Agent."
**Attribution**: Lenny Rachitsky
**What this source adds**: The definitive case study. 500+ reader submissions distilled to 50 non-technical use cases — from raffle-winner picking to competitor ad research to self-driving documentation — all served by a tool branded for developers. Helen Lee Kupp's testimonial is the clearest articulation of the identity barrier from a user who overcame it.
**Links**: [Original](https://www.lennysnewsletter.com/p/everyone-should-be-using-claude-code) | [Archive](../../sources/2026-02-13-everyone-should-use-claude-code-more.md)

## Related

- [Agent as Cross-Tool Workflow Hub](../horizontal/agents/system-design/agent-as-cross-tool-workflow-hub.md) — one of the use-case clusters demonstrating broad non-technical capability
- [Agent-Mediated Self-Reflection](../horizontal/agents/system-design/agent-mediated-self-reflection.md) — another novel use-case cluster from the same source
- [AI Disrupts Strategic PM Skills Most](ai-disrupts-strategic-pm-skills-most.md) — both are counterintuitive adoption insights from Lenny
- [Data Silos Block Enterprise Agent Adoption](data-silos-block-agent-adoption.md) — another adoption barrier, structural (data fragmentation) rather than perceptual (tool identity)
