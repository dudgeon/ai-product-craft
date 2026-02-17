---
title: "Everyone Should Be Using Claude Code More"
created: 2026-02-13
updated: 2026-02-14
template: templates/source.md
template_version: 3
tags: [source, ai-pm, newsletter]
status: processed
source_type: newsletter
source_url: "https://www.lennysnewsletter.com/p/everyone-should-be-using-claude-code"
archive_url: "domains/professional-development/ai-pm/sources/2026-02-13-everyone-should-use-claude-code-more.md"
author: "Lenny Rachitsky"
published: 2025-10-14
discovered: 2026-02-13
summary: "50 ways non-technical people use Claude Code — argues it's the best consumer AI product when reframed as 'Claude Local' or 'Claude Agent.' Core thesis: the word 'Code' is an adoption gate; the capability was always there for non-technical use cases. Use cases span lead gen, self-reflection, cross-tool workflows, documentation automation, writing, file management, and more."
domain: professional-development
project: ai-pm
---

# Everyone Should Be Using Claude Code More

**By**: Lenny Rachitsky
**Type**: newsletter
**URL**: https://www.lennysnewsletter.com/p/everyone-should-be-using-claude-code

## Summary

Lenny argues Claude Code is the best consumer AI product and that non-technical people should be using it far more. The key reframe: forget the word "Code" and think of it as "Claude Local" or "Claude Agent." It's a super-intelligent AI running locally, able to do stuff directly on your computer. Since it's on your machine, it can handle larger files, run longer than cloud chatbots, and has filesystem access that makes it uniquely capable.

Collects 50 creative non-technical use cases from 500+ reader submissions spanning sales/lead gen, self-reflection, cross-tool workflow automation, documentation, writing, file management, research, and personal life management.

## Key Ideas Extracted

- [Tool Identity as Adoption Gate](../knowledge-base/ai-adoption/tool-identity-as-adoption-gate.md) — the naming/positioning thesis
- [Agent as Cross-Tool Workflow Hub](../knowledge-base/horizontal/agents/system-design/agent-as-cross-tool-workflow-hub.md) — MCP integration pattern
- [Agent-Mediated Self-Reflection](../knowledge-base/horizontal/agents/system-design/agent-mediated-self-reflection.md) — agents as behavioral analysts
- [Knowledge Capture as Side Effect](../knowledge-base/horizontal/agents/system-design/knowledge-capture-as-side-effect.md) — enriched with self-maintaining documentation examples

## Notes

- Context from user: "for ai-pm"
- Published Oct 14, 2025 — one of the earliest mainstream "Claude Code for everyone" pieces
- Relevant to: Claude Code adoption patterns, non-technical AI usage, consumer AI product design, agent architecture patterns
- Helen Lee Kupp (#9) and Teresa Torres (#12) provide particularly rich individual testimonials
- Teresa Torres's writing workflow (#12) cross-referenced to her dedicated source files for future processing

## Raw Content

Ever since my chat with Dan Shipper, I couldn't stop thinking about his hot take that Claude Code was the most underrated AI tool for non-technical people. A few weeks ago, I finally started playing around with it, and holy sh*t, we've all been sleeping on Claude Code.

The key is to forget that it's called Claude Code and instead think of it as Claude Local or Claude Agent. It's essentially a super-intelligent AI running locally, able to do stuff directly on your computer—from organizing your files and folders to enhancing image quality, brainstorming domain names, summarizing customer calls, creating Linear tickets, and, as you'll see below, so much more.

Since it's running on your machine, it can handle much larger files, run much longer than the cloud-based Claude/ChatGPT/Gemini chatbots, and it's fast and versatile. Claude Code is basically Claude with superpowers.

To inspire your own ideas, I've collected 50 of my favorite and most creative ways non-technical people are using Claude Code in their work and life.

### Lenny's 5 personal use cases

1. Clearing space on computer — "How can I clear some storage on my computer?" then discuss options
2. Improving image quality of screenshots
3. Downloading YouTube videos
4. Downloading all images from a Google Doc in high-res
5. Picking random raffle winner from Google Sheet

### 50 creative use cases from readers

1. **Brainstorming domain names** (Ben Aiad) — suggest creative options across TLDs, verify availability
2. **Finding high-quality leads** (Jeff Lindquist) — "look at what I'm building and identify the top 5 companies in my area that would be good for a pilot"
3. **Scraping GitHub for leads** (Sergei Zotov) — search repos for sensitive data patterns to identify companies needing data masking; produces priority scores and LinkedIn URLs
4. **Noticing conflict avoidance** (Dan Shipper) — downloads all meeting recordings, asks Claude Code to identify times he's subtly avoided conflict
5. **System diagnostics** (Anthony Roux) — check load averages, memory pressure, disk space, stuck processes; faster than running commands manually
6. **Cleaning up invoice files** (Martin Merschroth) — reads each file, renames to "YYYY-MM-DD Vendor - Invoice - Product.pdf", moves to right folder
7. **Organizing files and folders** (Justin Dielmann) — find duplicates, organize downloads, review directory structure, find old files; "like having a thoughtful assistant who actually understands context"
8. **Building a slide tower for his son** (John Conneely) — built a DIY subagent for construction planning
9. **Organizing scattered thoughts** (Helen Lee Kupp) — "I'm a mom who voice-records ideas during morning stroller walks, not a developer. The terminal interface? Overwhelming at first. The word 'Code'... but what if I don't have a 'coding project'?" Fed it rambling voice notes → organized research themes → wrote article in her exact voice → created LinkedIn versions → everything ready to publish
10. **Writing job descriptions** (Justin Bleuel) — generated full JD, hiring plan, interview plan, and rubric for new role at Clay. Fed it internal hiring materials + competitor JDs.
11. **Synthesizing customer call transcripts** (Derek DeHart) — "my current Claude Code jam is synthesizing transcripts of calls with customers to compile evidence that supports or invalidates a running tally of assumptions/requirements/hypotheses. Given MCPs to interact with other tools in our productivity stack—Fireflies, Linear, Notion—it's become my hub for ongoing product research and development."
12. **Writing workflow** (Teresa Torres) — "I now write all of my content with Claude Code in VS Code. We iterate on an outline, it helps me improve the hook, it conducts research for me and adds citations to my outline, and it reviews and gives feedback on each section as I write."
13. **Audio file manipulation** (Dan Heller) — convert sample rates, rename, translate Portuguese to English
14. **Self-driving documentation** (James Pember) — "give an Agent the responsibility of figuring out how/where our documentation can be better and more comprehensive. Using Claude Code together with Playwright to automatically explore our software independently, identify knowledge gaps in our documentation, and then create those changes itself."
15. **Self-improving feedback loop** (Gang Rui) — slash command analyzes journal entries + git commits for past 7 days, spots gaps between stated intentions and actions, suggests system improvements. "Like having a COO that learns from my patterns."
16. **Competitor ad research** (Sumant Subrahmanya) — extract ads from competitors' ad library, find the problem/use case/copy that's working, repurpose
17. **Auto-generating changelogs** (Manik Aggarwal) — scans commits from time period, pulls in changelog guidelines, drafts structured changelog. Hours → 10-15 minutes.
18. **Building presentations** (Hank Yeomans) — all slides as HTML, uses template .md file for branding consistency, interactive browser-based presentations
19. **Social media research** (Danny Shmueli) — 4 custom subagents in .claude/agents/: Reddit replier, Reddit promoter, X specialist. One command → finds relevant threads → drafts replies.
20. **Roadmapping** (Abhi Chandwani) — "Because it has access to my repos, I am able to get a pretty good view on the impact vs. effort across the roadmap." Maintains a {project}-product repo with verbose git commits to create context for future agent workflows. CLAUDE.md has paths to engineering repos.

Plus additional use cases:
- Fully uninstalling Adobe products (Jonathan Stiansen)
- Automating Jira from call transcripts (Terry Lin) — "take a call transcript with my eng team, write up action items, create tickets in Jira using MCP—hands-off"
- Summarizing Intercom tickets → Asana bug reports (Eren Gündüz)
- PM tasks: Linear issues, release notes, UX improvements (Trist Adlington) — "I talk to Claude more than anyone else"
- Understanding codebase as new CPO (Brandon Dorman)
- Scheduling figure-drawing models via Gmail (Daniel Doubrovkine)
- Wi-Fi router configuration via Playwright (Chingis Alekenov)
- Doctor appointment audio → transcribed assistant (Iliya Valchanov)
- Photo portfolio PDF for daughter's school (Melvin Vivas)
- "Claude CEO" — daily briefing from Gmail + Brex + Mercury + Linear (Dennison Bertram)
- Research across arXiv papers (Troy Assoignon)
- Slack conversations → organic social posts (Chad Boyda)
- Reverse-building PRDs from code + conversations (Megan Salisbury)
- Resizing GIF, formatting NTFS SD card (Akilesh Bapu)
- Querying contract clauses across stored contracts (Pulkit Agrawal)

### Advanced use cases (linked, not detailed)
- Refining backlog in Linear
- Managing user research, concepts, test results, strategy
- Building attention command center
- Product discovery notes → PRDs → coding agent optimization
- Product messaging first drafts
- Standups, sprint retros, PRD reviews, career OS
- Running a branding studio, marketing, product, entire life

### Footnote

"Claude Code does not actually run 'locally' on your machine—the AI/LLM processing happens in the cloud—but you run the commands locally (directly on your machine), it has access to all of your local files and computer interfaces, and it's specifically designed to feel 'local.'"

---

[← Back to Source Registry](README.md)
