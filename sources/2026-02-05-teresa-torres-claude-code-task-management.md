---
created: 2026-02-05
updated: 2026-02-05
template: templates/source.md
template_version: 2
tags: [source, ai-pm-craft]
status: unread
source_type: article
source_url: "https://www.chatprd.ai/how-i-ai/teresa-torres-claude-code-obsdian-task-management"
archive_url: "domains/professional-development/ai-pm-craft/sources/2026-02-05-teresa-torres-claude-code-task-management.md"
author: "Claire Vo"
published: 2026-01-19
discovered: 2026-02-05
summary: "Teresa Torres built a Claude Code + Obsidian productivity system: custom /today command for daily task assembly, automated arXiv/Scholar research digests, and a granular context library ('lazy prompting') where dozens of small md files replace lengthy prompts. Core thesis: build your own AI tools, treat Claude as pair programmer for everything."
domain: professional-development
project: ai-pm-craft
---

# How I AI: Teresa Torres's Claude Code System for Task Management, Automated Research, and 'Lazy' Prompting

**By**: Claire Vo (interview with Teresa Torres)
**Source**: [ChatPRD - How I AI](https://www.chatprd.ai/how-i-ai/teresa-torres-claude-code-obsdian-task-management)
**Type**: article

## Summary

*Fill after reading. 2-3 sentences: what is this about, what's the core argument or insight?*

## Key Ideas Extracted

*Fill during processing. Each idea links to a knowledge entry.*

## Notes

*Your annotations, reactions, questions, disagreements. Written during or after reading.*

## Raw Content

Teresa Torres (author of Continuous Discovery Habits) has built a deeply integrated productivity system using Claude Code + Obsidian. Three core workflows:

**Workflow 1: Personalized Task Manager**
- Custom `/today` slash command triggers Python script that scans task files and assembles daily to-do list
- Every task is its own markdown file with YAML frontmatter (type, due_date, tags)
- Tasks created via natural language in Claude Code terminal
- Claude handles tagging using taxonomy defined in claude.md
- Output: daily markdown file with tasks due today, overdue, in-progress ideas, research digest

**Workflow 2: Automated Research Digest**
- Two Python cron jobs: morning search script (arXiv, Google Scholar) + nightly summarization script
- Config file with keywords/topics; tracks what's already been shown
- Claude generates detailed summaries focused on methodology and effect size
- New PDFs downloaded manually as a filter step; summaries appear next day in digest

**Workflow 3: 'Lazy Prompting' via Granular Context Library**
- Broke context into dozens of tiny, focused markdown files in an "LLM Context" Obsidian vault
- Uses index files as maps (e.g., business_profile.md tells Claude where to find specific context)
- Global claude.md routes: business question → business profile, personal → personal profile
- Built iteratively: at end of each session, asks "Claude, what'd you learn today that we should document?"
- Result: simple prompts produce high-quality output because context is pre-loaded and well-organized

**Key insight**: "pair programming for everything" — Claude Code as a true partner, not just a code tool. The most powerful AI applications may be the ones we build for ourselves.

**Referenced tools**: Claude Code, Obsidian, VS Code, Descript, Trello
**Teresa's links**: producttalk.org, justnowpossible.com (podcast), Continuous Discovery Habits (book)
