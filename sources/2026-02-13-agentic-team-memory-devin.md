---
title: "Agentic Team Memory: Knowledge That Writes Itself"
created: 2026-02-14
updated: 2026-02-14
template: templates/source.md
template_version: 3
tags: [source, ai-pm]
status: processed
source_type: article
source_url: "https://x.com/dabit3/status/2022459842342916559"
archive_url: "domains/professional-development/ai-pm/sources/2026-02-13-agentic-team-memory-devin.md"
author: "Nader Dabit (@dabit3)"
published: 2026-02-13
discovered: 2026-02-14
summary: "Devin (Cognition) captures engineering team knowledge as a side effect of corrections engineers already make — not by asking them to write docs. When an engineer corrects the agent, it suggests persisting the correction as a knowledge item. Knowledge also auto-generates from repos (READMEs, AGENTS.md, CLAUDE.md, .cursorrules), evolves via suggested updates, and scopes to repos or org-wide. The thesis: knowledge that writes itself is knowledge that stays current."
domain: professional-development
project: ai-pm
---

# Agentic Team Memory: Knowledge That Writes Itself

**By**: Nader Dabit (@dabit3), Cognition
**Source**: [X Article](https://x.com/dabit3/status/2022459842342916559)
**Type**: article (X long-form)

## Summary

Every engineering team has tribal knowledge that wikis and READMEs fail to capture because documentation always loses to shipping. Devin (Cognition's AI agent) solves this by making knowledge capture a side effect of corrections engineers are already making — not a separate documentation task. The result: a self-maintaining knowledge base that new engineers inherit automatically.

## Key Ideas Extracted

- [Knowledge Capture as Side Effect](../knowledge-base/horizontal/agents/system-design/instruction-design/knowledge-capture-as-side-effect.md) — Design agent correction loops to double as knowledge capture pipelines; capture from corrections, repo scanning, and suggested updates
- [Self-Maintaining Knowledge Bases](../knowledge-base/ai-adoption/self-maintaining-knowledge-bases.md) — Agent-mediated capture solves documentation staleness; emergent onboarding, tribal knowledge externalization, quality improves with team scale

## Key Concepts

### Knowledge as Side Effect
When an engineer corrects the agent ("don't call fetch directly, use the wrapper"), Devin suggests saving that as a knowledge item. The engineer reviews and tweaks, and from that point every future session across the org retrieves it when relevant. No documentation mindset required — just correct the agent like you'd correct a teammate.

### Multiple Knowledge Sources
- **Chat corrections**: Most organic source — corrections during normal work
- **Auto-generated from repos**: Devin scans READMEs, file structure, AGENTS.md, CLAUDE.md, .cursorrules, .rules files
- **Suggested updates**: Devin proposes updates to existing knowledge items as conventions evolve
- **Manual creation**: Direct creation via UI or API for upfront codification

### Scoped Knowledge
Knowledge can be pinned to a specific repo or applied org-wide. Backend deployment conventions don't surface when working on the marketing site. Org-wide standards (commit message format) apply everywhere. This prevents context pollution.

### Emergent Onboarding
Nobody writes an onboarding guide — it emerges from accumulated corrections. A new engineer starts a session and the agent already knows every team convention. This also lowers the barrier for non-technical contributors by providing more guardrails.

## Notes

- Direct parallel to home-brain's retro pattern: after friction, surface findings and propose instruction updates. Devin automates this loop.
- The "knowledge as side effect" pattern is what CLAUDE.md auto-memory already does in a limited way — corrections become persistent instructions. Devin scales this to teams.
- The multi-source approach (chat + repo scanning + suggested updates) is more comprehensive than most agent memory solutions that only capture from one channel.
- Interesting contrast with ClawVault source: ClawVault is filesystem-native memory for general agents; Devin's approach is correction-driven memory for engineering teams. Different entry points, similar end state (self-maintaining knowledge base).
- Scoped knowledge (repo-level vs org-wide) is an access control pattern worth tracking — relates to the Mernit/Openclaw "unix permissions as governance" idea.
- The core thesis — "knowledge that writes itself is knowledge that stays current" — is a strong framing for why traditional documentation fails and agent-mediated capture succeeds.

## Raw Content

Every engineering team has tribal knowledge. Most teams try to capture this in wikis, READMEs, or onboarding docs. These go stale fairly quickly. Nobody maintains them because the cost of writing documentation always loses to the cost of shipping features.

At Cognition, they capture knowledge from corrections engineers are already making instead of asking people to write docs. When an engineer says "don't call fetch directly, use the wrapper in src/lib/api-client", Devin suggests saving that as a knowledge item. The engineer reviews it, tweaks the wording if needed, and saves. From that point on every future session across the org retrieves that knowledge when relevant.

Chat feedback is the most organic source, but knowledge also gets created from auto-generated repo scans (READMEs, file structure, AGENTS.md, CLAUDE.md, .cursorrules, .rules files), suggested updates to existing items as conventions evolve, and manual creation via UI or API.

The team's conventions, deployment quirks, internal library preferences, and common pitfalls accumulate organically. A new engineer joins, starts a session, and the agent already knows every convention the team has built up. Knowledge can be pinned to a specific repo or applied org-wide — backend deployment conventions don't surface when working on the marketing site.
