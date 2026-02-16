---
title: "CJ Hess on Building Custom Dev Tools and Model-vs-Model Code Reviews"
created: 2026-02-15
updated: 2026-02-16
template: templates/source.md
template_version: 3
tags: [source, ai-pm, claude-added]
status: unread
source_type: podcast
source_url: "https://www.chatprd.ai/how-i-ai/cj-hess-tenex-custom-dev-tools-and-model-vs-model-code-reviews"
archive_url: ""
author: "CJ Hess"
host: "Claire Vo"
published: 2026-02-09
discovered: 2026-02-15
summary: "Software engineer CJ Hess (Tenex) demonstrates two workflows: (1) Flowy, a custom-built visual planning tool that renders JSON as interactive diagrams and UI mockups, bridging human visual intuition with Claude Code's textual understanding — he uses custom skills to have Claude generate flowcharts and mockups, then iterates visually before building features; (2) a model-vs-model code review workflow using GPT-5.2 Codex (aliased as 'carl') to act as a critical staff engineer reviewing Claude's code, checking for correctness against plan artifacts, code smells, and refactoring opportunities."
domain: professional-development
project: ai-pm
# taxonomy_inference: horizontal/agents (custom-tool-building, agent-tooling); software-methodology (compound-engineering)
# provenance: bulk-added by Claude from podcast-episode-compilation.md (2026-02-15)
# rescrape_needed: false — full article scraped from ChatPRD 2026-02-16
---

# CJ Hess on Building Custom Dev Tools and Model-vs-Model Code Reviews

**By**: CJ Hess
**Host**: Claire Vo
**Source**: [How I AI (ChatPRD)](https://www.chatprd.ai/how-i-ai/cj-hess-tenex-custom-dev-tools-and-model-vs-model-code-reviews)
**Type**: podcast

## Summary

CJ Hess, a software engineer at Tenex, demonstrates two powerful AI engineering workflows. First, he built Flowy, a custom visual dev tool that takes JSON definitions and renders them as clean, interactive diagrams and UI mockups — solving the problem of messy ASCII flowcharts from LLMs. He uses custom Claude Code skills (simple markdown files defining the JSON schema) to have Claude generate flowcharts and mockups, iterates visually in the Flowy web UI, then directs Claude to build features based on the visual artifacts. Second, he uses a multi-model "trust but verify" approach: Claude (aliased as "kevin") handles creative feature building, then GPT-5.2 Codex (aliased as "carl") performs rigorous code review as a "curmudgeonly staff engineer." He feeds Codex a structured review prompt checking for correctness against plan artifacts, code smells, and refactoring opportunities. Codex caught a subtle visual bug, missing useEffect dependencies, and suggested component extraction — then implemented its own fixes. This multi-model workflow lets you get high velocity from one model and quality assurance from another.

## Key Ideas Extracted

- **Build your own dev tools when off-the-shelf doesn't fit**: CJ built Flowy because ASCII flowcharts from LLMs were too messy — the era of bespoke developer tools built cheaply with AI is here
- **JSON as bridge between visual and textual**: Flowy renders JSON as visual diagrams while keeping the underlying format perfectly readable for Claude — a clean interface between human visual intuition and AI's textual understanding
- **Custom skills as simple markdown documentation**: The skill.md file that teaches Claude how to use Flowy is just a markdown file defining JSON schema, styles, colors, and examples — lightweight but powerful
- **Visual iteration before building**: Edit diagrams directly in the Flowy UI, then point Claude back at the updated file — visual planning artifacts provide enough context to skip detailed markdown plans
- **Multi-model "trust but verify"**: Use Claude for creative, collaborative coding and Codex for critical, analytical code review — different models playing different roles like team members
- **Structured code review prompts**: Ask the reviewer model three specific things: (1) does code match plan artifacts, (2) general code smells, (3) strategic refactoring suggestions
- **Model-vs-model catches subtle bugs**: Codex found a visual bug where a spinner pointer landed between dots instead of on dots, plus missing useEffect dependencies — issues that vibe coding alone would miss
- **Terminal aliases for different AI personas**: "kevin" for Claude Code, "carl" for Codex — simple ergonomic pattern for switching between AI tools with different roles

## Notes

This is CJ Hess's second appearance on How I AI (first was the Flowy/Codex QA episode from 2025-12-16). This episode provides much more detail on the Flowy workflow and the model-vs-model code review pattern. The "build your own tools" message is central — when a tool doesn't fit your mental model, build one that does using AI. The multi-model quality control pattern (creative model + critical model) is a significant workflow pattern worth tracking as a distinct practice.

## Raw Content

CJ Hess is a software engineer at Tenex doing innovative work in AI engineering. He's not just using AI to write code — he's building his own ecosystem of tools to make the development process more intuitive and powerful.

In the early days of software engineering, customizing your environment meant picking an IDE and maybe some linters. Now, we're in an era where you can build bespoke tools for yourself, cheaply and quickly, that are tailored to your exact workflow.

### Workflow 1: Visual Planning and Feature Building with Flowy

**Problem**: LLMs are great at generating plans in Markdown, but their ASCII flowcharts are messy and hard to interpret. "There's always this misalignment of that edge character."

**Solution**: Flowy — a custom-built dev tool that takes a JSON definition and renders it as a clean, visual, interactive diagram. A bridge between human visual intuition and AI's textual understanding.

**Step 1: The Initial Idea and Prompt**

CJ wanted to replace a static "Tips & Tricks" section with an interactive spinning wheel. He used a custom terminal alias `kevin` (Claude Code with bypass permissions) and prompted for both the feature description and explicit instructions to use the "flowy flowchart skill" to create animation timing and user flow diagrams.

**Step 2: Generating Flowcharts with a Custom Skill**

Claude Code, guided by a custom skill (a simple markdown file defining JSON schema for nodes/edges, available styles, colors, and examples), generated two JSON files. Viewed in the Flowy web app, these become clear, readable diagrams.

The skill itself (skill.md) was developed iteratively. It acts as documentation that teaches Claude how to use Flowy correctly.

**Step 3: Iterating Visually and Generating UI Mockups**

The interactive loop: CJ noticed the animation was 3 seconds instead of desired 4 seconds. Instead of editing JSON manually, he edited the diagram directly in the Flowy UI (which updates the underlying file), then pointed Claude back at the file to acknowledge the change.

Then asked Claude to create UI mockups based on the diagrams — Claude generated a Flowy file visualizing the spinner wheel in different states (before, during, after spin).

**Step 4: From Visual Plan to Live Feature**

With detailed flowcharts and UI mockups complete, CJ gave a simple command: "Based on the flowcharts and the mockups, build this feature." Because the planning artifacts were so clear and specific, Claude implemented the feature correctly — a working spinner wheel behaving exactly as designed in the Flowy diagrams.

### Workflow 2: Quality Control with Model-vs-Model Code Reviews

**Problem**: "Claude is very eager sometimes and maybe jams things in there without thinking about the bigger picture." Vibe coding can lead to technical debt.

**Solution**: Use GPT-5.2 Codex (aliased as `carl`) to review Claude's code. Treat Codex like a critical, experienced staff engineer. Claude is more "delightful" and "steerable" for creative coding; Codex provides rigor for code review.

**Step 1: Kicking Off the Review with 'Carl'**

After Claude built the spinner feature, CJ invoked Codex with a structured review prompt:
1. Does the code accurately reflect the plan/diagram artifacts?
2. Are there any general code smells?
3. If we were to do this again and take a different approach to refactor code around it to overall improve this code base, what approach would be best?

**Step 2: Analyzing the Feedback**

Codex returned a detailed, insightful report:
- **Discrepancy**: Noticed the spinner's pointer was designed to land on a dot (per mockup) but was landing between dots in the implementation
- **Code Smells**: Missing dependencies in a useEffect hook
- **Refactoring Opportunities**: Suggested pulling out logic into separate components and defining constants

This is the kind of feedback that prevents small vibe-coded features from degrading codebase health over time.

**Step 3: Implementing the Fixes**

Simple follow-up: "great, please make those improvements." Codex refactored the code, fixing bugs and implementing its own suggestions — closing the loop with a feature that was both functionally correct and well-structured.

### Key Themes

Two transformative ideas: (1) Build your own developer tools — if a tool doesn't fit your mental model, build one that does; (2) The "trust but verify" model using multiple AIs is powerful — leverage creative strengths of one model and critical strengths of another to build at high velocity without sacrificing quality. Assemble your own AI team with different members playing different roles.
