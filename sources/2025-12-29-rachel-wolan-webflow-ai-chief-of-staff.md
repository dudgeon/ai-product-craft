---
title: "Webflow CPO Rachel Wolan's AI Chief of Staff & Org Adoption Playbook"
created: 2026-02-15
updated: 2026-02-16
template: templates/source.md
template_version: 3
tags: [source, ai-pm, claude-added]
status: unread
source_type: podcast
source_url: "https://www.chatprd.ai/how-i-ai/webflow-cpo-ai-chief-of-staff-adoption-playbook"
archive_url: ""
author: "Rachel Wolan"
host: "Claire Vo"
published: 2025-12-29
discovered: 2026-02-15
summary: "Rachel Wolan (CPO, Webflow) walks through three workflows: (1) a custom AI Chief of Staff app running locally via Claude Code that connects to Google Calendar and Gmail APIs for daily triage, delegation suggestions, and a 'Brutal Truth' module that tells her she's operating as a senior PM instead of a CPO; (2) an on-demand networking event prep system that uses vision/OCR on a guest list screenshot, runs multi-step research (web + LinkedIn), and generates personalized talking points using markdown knowledge base files; (3) a company-wide 'Builder Day' playbook for AI adoption that drove Cursor usage among designers from near-zero to 50% sustained adoption."
domain: professional-development
project: ai-pm
# taxonomy_inference: horizontal/agents (custom-agent-building); ai-adoption (executive-adoption, tool-building)
# provenance: bulk-added by Claude from podcast-episode-compilation.md (2026-02-15)
# rescrape_needed: false — full article scraped from ChatPRD 2026-02-16
---

# Webflow CPO Rachel Wolan's AI Chief of Staff & Org Adoption Playbook

**By**: Rachel Wolan
**Host**: Claire Vo
**Source**: [How I AI (ChatPRD)](https://www.chatprd.ai/how-i-ai/webflow-cpo-ai-chief-of-staff-adoption-playbook)
**Type**: podcast

## Summary

Rachel Wolan, Chief Product Officer at Webflow, demonstrates three workflows that embody the AI-native executive approach. First, she built a custom "AI Chief of Staff" application running on her local machine via Claude Code, connected to Google Calendar and Gmail APIs with intentionally limited permissions (read-only calendar, read/archive/label/draft-only email). Each morning she prompts it to review her day and suggest delegations — it identifies meetings to make async, tasks to delegate to directors, and optional invites to decline. A unique "Brutal Truth" module provides unvarnished feedback on how she's spending her time. Second, she uses a multi-step research agent for networking event prep: drop in a screenshot of a guest list, the system uses vision/OCR to extract names, then runs web search + LinkedIn search + targeted news search for each person, combining results with her personal markdown knowledge base (about_me.md, webflow_products.md) to generate a comprehensive prep document with priority connections, personalized conversation starters, and hot topics. Third, she shares her playbook for company-wide "Builder Days" — structured events with curated tool access, function-specific tracks, dedicated Slack support, warm-up exercises, judging panels, and prizes. After the first Builder Day, Cursor usage among designers went from near-zero to approximately 50% sustained adoption.

## Key Ideas Extracted

- **"Brutal Truth" module for executive accountability**: Programming an AI agent to deliver unvarnished feedback about time allocation provides the kind of honest coaching even human chiefs of staff hesitate to give
- **Permission guardrails by design**: Read-only calendar, draft-only email (never send) — intentionally limiting agent permissions prevents mistakes while maintaining utility
- **Markdown-powered personal knowledge base**: Simple .md files (about_me.md, webflow_products.md) provide personalization context without needing a complex database — low-tech, high-value approach
- **Vision/OCR for low-fi input**: Dropping a screenshot of a guest list into an agent that extracts names via OCR eliminates manual data entry for networking prep
- **Multi-step research chains**: Web search + LinkedIn + targeted news search per person mimics what a human would do but completes it for a dozen people in minutes
- **Builder Day structure for adoption**: Curated tool access, function-specific tracks, dedicated support channels, warm-up exercises, judging panels, and prizes create a motivating environment that overcomes adoption friction
- **Measured adoption outcomes**: Tracking tool usage before and after Builder Day with a Hex dashboard showed Cursor design adoption went from near-zero to ~50% sustained — moving the team from "laggard" to "early majority"
- **Personal experience builds leadership credibility**: Building your own tools gives you the authenticity to lead organizational change — "improve yourself, then empower your team"

## Notes

This is one of the strongest episodes for executive-level AI adoption patterns. The AI Chief of Staff concept (local app, API connections, intentional permission constraints, "brutal truth" module) is a replicable architecture. The Builder Day playbook pairs well with Brian Greenbaum's Pendo episode as complementary approaches to organizational AI adoption — Greenbaum's is more grassroots/ongoing, Wolan's is more event-driven/top-down.

## Raw Content

Rachel Wolan, CPO at Webflow, embodies the AI-native executive. She started coding at 16 and has returned to her builder roots. She walked through the custom "AI Chief of Staff" application she built — a personalized tool that helps manage the relentless pace of an executive schedule. Plus her detailed playbook for running company-wide "Builder Days."

### Workflow 1: Building a Personal AI Chief of Staff for Daily Triage

**Problem**: The sheer volume of information and commitments facing an executive. Prepping for meetings just minutes beforehand ("just-in-time executive").

**Step 1: Connecting the Dots with APIs**
- Google Calendar API and Gmail API connections
- API tokens stored securely in .env file
- **Intentionally limited permissions**: Calendar is read-only; Gmail limited to reading, archiving, labeling, and creating drafts (not sending emails directly)

**Step 2: The Morning Calendar Review & Delegation Prompt**
Simple terminal prompt via Claude Code: "Tell me about my day tomorrow. What can I delegate?"

Agent returns prioritized suggestions:
- **Make Meetings Async**: Identifies meetings that could be handled via document or Slack update
- **Delegate Tasks**: Suggests specific meetings for directors to cover, even drafting the message
- **Decline Optional Invites**: Flags meetings from unknown organizers or with unclear agendas

**Step 3: Getting the "Brutal Truth"**
A unique programmed module for direct, accountable feedback. After analyzing the calendar, the agent delivered: "You're operating as a senior PM, not a CPO. You're reviewing PRDs, approving scripts, and recording marketing videos... The only thing that will matter in six months is [a specific strategic conversation]."

**Step 4: Email Triage**
Managing a 500+ deep inbox:
- **Archive ruthlessly**: Newsletters and non-essential communications
- **Highlight what's important**: Emails where someone is waiting on her for a document or decision
- **Draft responses**: Prepared replies for recurring requests or partnership inquiries

### Workflow 2: On-Demand Prep for Meetings and Networking Events

**Step 1: Ingesting a Guest List with Vision**
Drop a screenshot of a dinner guest list into the app. The model uses vision capabilities to perform OCR, extracting names of every attendee.

**Step 2: Multi-Step Research Agent**
For each extracted name:
- Initial web search for broad overview
- LinkedIn search for professional profile, current role, career history
- Deeper targeted web search for recent news, articles, or talks

**Step 3: Markdown-Powered Knowledge Base**
Agent is fed personal markdown files for personalization:
- `about_me.md`: Professional bio, communication style, career highlights
- `webflow_products.md`: Auto-generated monthly from release notes, detailing latest products and features

**Step 4: Final Prep Document**
Comprehensive output including:
- **Priority Connections**: Most relevant people to speak with
- **Personalized Conversation Starters**: Tailored opening lines based on their background and hers
- **Hot Discussion Topics**: Relevant industry trends (e.g., Answer Engine Optimization)
- **Venue Information**: Restaurant details for easy reference

### Workflow 3: The Playbook for Driving Org-Wide AI Adoption (Builder Days)

**Step 1: Setting the Stage**
Goal: Get people over the initial friction hump.
- **Tool Access**: Curated set — Cursor for coding, Figma for design, Make for automation, Webflow
- **Dedicated Tracks**: Different assignments for various functions (Product, Design, Data Science, User Research)
- **Support Channels**: Dedicated Slack channel staffed with engineers for troubleshooting

**Step 2: Making it Fun and Engaging**
- **Warm-up Assignment**: Simple exercise to get comfortable before the main project
- **Judging Panel**: Rachel and the CEO reviewed projects (friendly competition)
- **Prizes & Recognition**: Winners awarded in different categories

**Step 3: Measuring the Impact**
Used a Hex dashboard to track tool adoption before and after. Results: Cursor usage among the design team went from near-zero to ~50% adoption, sustained in following weeks. Moved a significant portion of the team from "laggard" to "early majority" on the adoption curve.

Post-event survey: participants found the day "fun, empowering, motivating, and eye-opening."

### Key Takeaway

The blueprint for the modern AI-native executive: start with a personal commitment to building tools that solve your own problems, then use that hands-on experience as authenticity and credibility to lead organizational adoption. Improve yourself, then empower your team.
