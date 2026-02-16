---
title: "GPT-5.3 Codex vs. Claude Opus 4.6 — Shipping 44 PRs in 5 Days"
created: 2026-02-15
updated: 2026-02-16
template: templates/source.md
template_version: 3
tags: [source, ai-pm, claude-added]
status: unread
source_type: podcast
source_url: "https://www.chatprd.ai/how-i-ai/gpt-5-3-codex-vs-claude-opus-4-6"
archive_url: ""
author: "Claire Vo"
host: ""
published: 2026-02-13
discovered: 2026-02-15
summary: "Claire Vo puts OpenAI's GPT-5.3 Codex and Anthropic's Claude Opus 4.6 head-to-head on real engineering tasks — a full marketing site redesign and a complex component refactoring — shipping 44 PRs, 98 commits, and 92,000+ lines of code in 5 days. Opus 4.6 excels at creative greenfield work (better planning, takes feedback effectively, produced a superior site redesign), while Codex excels as a rigorous code reviewer (found edge cases, architectural issues, and hardened code for production). Her recommended stack: Opus builds, Codex reviews."
domain: professional-development
project: ai-pm
# taxonomy_inference: software-methodology (model-selection, compound-engineering)
# provenance: bulk-added by Claude from podcast-episode-compilation.md (2026-02-15)
# rescrape_needed: false — full article scraped from ChatPRD 2026-02-16
---

# GPT-5.3 Codex vs. Claude Opus 4.6 — Shipping 44 PRs in 5 Days

**By**: Claire Vo
**Source**: [How I AI (ChatPRD)](https://www.chatprd.ai/how-i-ai/gpt-5-3-codex-vs-claude-opus-4-6)
**Type**: podcast

## Summary

Claire Vo tests OpenAI's GPT-5.3 Codex and Anthropic's Claude Opus 4.6 head-to-head on real, complex engineering work, resulting in 44 pull requests, 98 commits, and 92,000+ new lines of code in five days. Two major workflows: (1) A complete marketing site redesign where Codex was too literal and overfitted to individual feedback prompts (producing copy like "A dense product workflow"), while Opus 4.6 in Cursor demonstrated better planning, took aspirational feedback effectively, and produced a polished on-brand redesign that will ship. (2) A multi-model "dream team" workflow for refactoring MCP connector components — Opus 4.6 builds the first draft (80-90% there, functional and fast), then Codex reviews as a "principal engineer" finding edge cases, architectural issues, and code quality problems before implementing its own fixes. She frames the two models as complementary team members: Opus is the eager product engineer who builds quickly, Codex is the meticulous principal engineer who hardens code for production. Also covers Opus 4.6 Fast (~$150/million output tokens, 6x standard cost) and "token abundance" mindset — the ROI of shipping 44 PRs vastly exceeds model costs.

## Key Ideas Extracted

- **Models as team members, not competitors**: Opus 4.6 is the eager product engineer (creative, generative, greenfield), Codex is the meticulous principal engineer (code review, architectural analysis, edge cases)
- **Opus 4.6 wins on creative work**: Better planning, better at interpreting high-level briefs, responds well to aspirational feedback ("I want it to look like I spent a million dollars"), applies design consistently across pages
- **Codex is too literal for creative tasks**: Overfits to individual instructions without nuance or creative interpretation — when asked for "content-dense" site, it produced "A dense product workflow" headline
- **Multi-model build-then-review workflow**: Opus builds the first draft (80-90% complete), Codex performs rigorous code review identifying high-impact issues and edge cases, then implements its own fixes
- **Harness matters**: Cursor's planning mode and to-do list structure help get the best out of models — the tool you use affects model performance
- **Codex app's Git-first UX**: OpenAI's Codex desktop app centers Git concepts (repos, branches, work trees, diffs) and elevates Skills/Automations — good for both experienced engineers and learners
- **"Token abundance" mindset**: Opus 4.6 Fast at ~$150/M output tokens is expensive, but shipping 44 PRs that would traditionally take a team months makes the ROI obvious
- **Structured review prompts**: Ask the review model to check architecture, performance, scalability, and customizability — then let it implement its own suggestions

## Notes

This episode directly complements the CJ Hess model-vs-model episode (2026-02-09). Both independently converge on the same pattern: use Claude for creative building and a second model (Codex) for rigorous code review. Claire's framing of "eager product engineer + meticulous principal engineer" is a memorable mental model. The 44 PRs / 92K lines / 5 days stat is a concrete data point for the productivity acceleration narrative. Published date is Feb 13 based on article text (written Feb 15 in our file — corrected to Feb 13).

## Raw Content

The past week has been a whirlwind of new releases, with OpenAI dropping their Codex desktop app and the new GPT-5.3 Codex model, and Anthropic following with Claude Opus 4.6 and Opus 4.6 Fast. Claire put them through real, complex tasks to see where they shine and where they fall apart.

Results: 44 pull requests, 98 commits, and over 92,000 new lines of code shipped in five days.

### Workflow 1: The Ultimate Website Redesign Showdown

**Task**: Complete redesign of the ChatPRD marketing site, moving from PLG to PLG+enterprise positioning.

**GPT-5.2 Codex in the Codex App**

The Codex desktop app centers core Git concepts (repos, branches, work trees, diffs) and makes Skills/Automations first-class features. However, Codex proved too literal for the creative task:
- High-level prompt given with creative freedom to redesign
- Codex followed instructions blindly without nuance or creative interpretation
- Explicitly wrote copy like "If you're here for product-led growth, click here... If you are here as an enterprise customer, click here"
- Overfitted to feedback: when asked for more about integrations, the entire page became about integrations
- When asked for a more content-dense site like Hex's, produced headline: "A dense product workflow for AI powered teams"
- End result: redesigned homepage and enterprise page only (not the full site), solid code but poor design and copy

**Claude Opus 4.6 in Cursor**

Same task, dramatically different result:
- Better at planning and executing the long-running task
- Explored the codebase, created a plan, built components independently
- Initial design was "Tailwind Indigo AI slop" — generic and unsophisticated
- After aspirational feedback ("I want it to look like I spent a million dollars"), Opus acknowledged and came back with a stunning redesign
- Integrated existing brand aesthetic, used real colors and relevant graphics instead of placeholders
- When asked to apply styles to rest of site, did so consistently across pricing page and other sections
- This is the version they're likely to ship

**Verdict**: For creative greenfield work, Opus 4.6 was the clear winner.

### Workflow 2: The Dream Team — Opus for Building, Codex for Reviewing

**Task**: Refactor messy MCP connector components (GitHub, Linear, etc.) — inconsistent code, hard to maintain, needed clean/reusable/customizable solution.

Mimics the dynamic of an eager product engineer paired with a seasoned principal engineer.

**Step 1: Build the First Draft with Opus 4.6**

Tasked Opus in Cursor with refactoring tool components. Created a sensible, flexible component structure. Result was 80-90% of the way there — functional, looked great, massive improvement. Opus is the engineer who just gets stuff done and builds things quickly.

**Step 2: Review and Harden with Codex**

Took the code to the Codex app. Prompted for principal-level code review checking architecture, performance, scalability, and customizability. Codex was phenomenal — tore the code apart identifying high-impact issues and edge cases that Opus missed. Prioritized issues, asked clarifying questions, then implemented fixes and polished to production-ready state. Code passed AI-powered Bugbot review (also running on a Codex model) and shipped.

"GPT-5.3 Codex replicates the principal software engineer experience perfectly: you might have to fight them tooth and nail to build something new, but they are more than happy to find every single flaw in someone else's code."

### Speed, Cost, and Token Abundance

Opus 4.6 Fast is incredibly fast but roughly 6x the cost of standard (~$150/million output tokens). With "token abundance" mindset: shipping 44 PRs and major features would traditionally take a team months and cost tens of thousands — even at high model costs, the value and velocity are off the charts. Caveat: "don't pick the wrong task" for the fast model, or you'll get a bill you're not happy with.

### Recommended AI Engineering Stack

- **Claude Opus 4.6**: Creative, generative, greenfield work — new features, UI design, initial implementation. The eager product engineer.
- **GPT-5.3 Codex**: Code review, architectural analysis, finding edge cases. The meticulous principal engineer ensuring code is hardened, scalable, and production-ready.
- **Combined**: Let Opus build it, then let Codex break it.
