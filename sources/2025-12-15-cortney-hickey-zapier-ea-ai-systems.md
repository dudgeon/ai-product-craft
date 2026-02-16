---
title: "Zapier EA Cortney Hickey's 4 AI Workflows for Meeting Prep, Culture Reinforcement, and Strategy"
created: 2026-02-15
updated: 2026-02-16
template: templates/source.md
template_version: 3
tags: [source, ai-pm, claude-added]
status: unread
source_type: podcast
source_url: "https://www.chatprd.ai/how-i-ai/ea-ai-workflows-for-meetings-culture-and-strategy"
archive_url: ""
author: "Cortney Hickey"
host: "Claire Vo"
published: 2025-12-15
discovered: 2026-02-15
summary: "Cortney Hickey (EA to CEO at Zapier) walks through four AI workflows that transform traditional EA work into scalable organizational systems: (1) an automated weekly meeting prep agent using Zapier Agents that eliminated a 2-hour Friday task, (2) an AI meeting coach that analyzes transcripts against company culture pillars to deliver personalized Slack feedback, (3) a custom GPT for stress-testing executive proposals with 278+ employees using it, and (4) a Google NotebookLM strategy companion that makes company strategy interactive and accessible to all employees."
domain: professional-development
project: ai-pm
# taxonomy_inference: ai-adoption (org-change, scaling-expertise); horizontal/agents (workflow-automation)
# provenance: bulk-added by Claude from podcast-episode-compilation.md (2026-02-15)
# rescrape_needed: false — full article scraped from ChatPRD 2026-02-16
---

# Zapier EA Cortney Hickey's 4 AI Workflows for Meeting Prep, Culture Reinforcement, and Strategy

**By**: Cortney Hickey
**Host**: Claire Vo
**Source**: [How I AI (ChatPRD)](https://www.chatprd.ai/how-i-ai/ea-ai-workflows-for-meetings-culture-and-strategy)
**Type**: podcast

## Summary

Cortney Hickey, Executive Assistant to the CEO at Zapier, demonstrates four AI workflows that shift the EA role from tactical support to strategic partner. Workflow 1: An automated weekly meeting prep agent built in Zapier Agents that triggers every Friday at 8 AM, scans the calendar, performs multi-source research (web, HubSpot CRM, Gmail, Slack) on external meeting participants, and delivers results as both Todoist tasks (scheduled 2 hours before each meeting) and a Slack digest — eliminating a recurring 2-hour manual task. Workflow 2: An AI meeting coach that ingests transcripts from Fellow, analyzes each participant's contributions against Zapier's cultural framework (values, meeting norms, "Five Dysfunctions of a Team," impact behaviors), and sends personalized coaching feedback via Slack DM. Workflow 3: A custom GPT ("Exec Prop") loaded with strategy memos, revenue roadmap, proposal examples, team norms, and CEO communication preferences — employees upload draft proposals and receive structured feedback with strengths/weaknesses, specific advice, example rewrites, and a bold coaching question. 278+ employees have used it. Workflow 4: A Google NotebookLM strategy companion aggregating all strategic documents, All-Hands transcripts, and org action plans into a conversational knowledge base where anyone can ask questions in natural language.

## Key Ideas Extracted

- **"Progress over perfection" for agent building**: Start with a simple digest, then iteratively add capabilities (CRM lookup, Slack search, LinkedIn links) as you learn what's useful
- **Multi-source research agents eliminate manual context-gathering**: Combining calendar + web + CRM + email + Slack into one automated flow replaces hours of pre-meeting prep
- **AI as cultural coaching at scale**: Using meeting transcripts analyzed against explicit cultural frameworks provides consistent, unbiased feedback that would be awkward for humans to deliver directly
- **Iteration on AI tone matters**: Initial cultural feedback was too soft; Cortney tuned the prompt to balance "demanding and supportive" for more actionable coaching
- **Custom GPTs as executive thought-process clones**: Loading a GPT with strategy docs, proposal examples, and CEO communication preferences lets anyone stress-test documents before executive review — 278 employees used it
- **When documents become clear enough, meetings get skipped**: The best outcome of the proposal GPT is that well-refined docs sometimes eliminate the need for the meeting entirely
- **NotebookLM as interactive strategy companion**: Aggregating strategic documents into a conversational knowledge base lets every employee understand how their role connects to company strategy
- **EA role as systems builder, not task executor**: AI enables EAs to build scalable organizational infrastructure rather than performing repetitive individual tasks

## Notes

One of the most practical episodes in the series — all four workflows are highly replicable. The culture-coaching workflow is a novel pattern worth tracking: using AI to systematically reinforce organizational values through meeting behavior analysis. The "Exec Prop" custom GPT pattern (loading organizational context + communication preferences into a GPT for document pre-review) is broadly applicable beyond the EA use case.

## Raw Content

This is one of the most practical, time-saving, and stress-saving conversations we've ever had on the show. We're talking about the operational backbone of a company — all the manual, repetitive work — and how AI can turn it into something automated and strategic.

Cortney Hickey is the Executive Assistant to the CEO at Zapier. Working at an automation company means she's on the front lines of using AI to optimize her role. She's building systems that not only give her hours back every week but also scale the effectiveness of the entire executive team and reinforce the company's culture.

AI is a tool for immense leverage. It lets her work herself out of the boring, repetitive tasks so she can focus on higher-impact, more interesting strategic work. It's a mindset shift from if you should use AI to when and how.

### Workflow 1: The Automated Weekly Meeting Prep Agent

**Problem**: Friday afternoon, staring at next week's calendar, trying to figure out who you're meeting, why, and what to prepare. Cortney used to block off two hours every Friday for this.

**Solution**: Custom agent built in Zapier Agents that mimics her exact manual steps.

**Process**:
- **Scheduled Trigger**: Automatically kicks off at 8:00 AM every Friday
- **Calendar Scan**: Reads Google Calendar for upcoming week, identifies meetings requiring preparation, filters out routine internal stand-ups/one-on-ones to focus on external or high-stakes meetings
- **Multi-Source Research**: For each external participant:
  - Web search for current role, industry experience, noteworthy public information
  - Connects to HubSpot CRM for existing relationship, recent sales notes, deal status
  - Searches Gmail and Slack for prior conversations or mentions
- **Dual Outputs**:
  - *Actionable Tasks*: Creates individual Todoist tasks for each meeting, populated with full research brief, scheduled to appear 2 hours before the meeting
  - *Weekly Digest*: Structured Slack digest summarizing key meetings, intelligence gathered, and suggested focus areas

**Key insight**: "Progress over perfection" — started with just a quick digest, then iteratively added capabilities. Using the built-in copilot, she can type natural language instructions like "for each participant, also add a LinkedIn hyperlink within the Slack digest" and the agent updates its own logic.

### Workflow 2: Reinforcing Company Culture with an AI Meeting Coach

**Problem**: Company values exist on paper but aren't consistently practiced day-to-day.

**Solution**: Automated system that turns meeting transcripts into coaching feedback.

**Process**:
- **Ingest Transcript**: Triggers after meeting concludes, pulling full transcript and metadata from Fellow
- **Apply Filters**: Ignores meetings under 10 minutes or those with external participants
- **Provide Deep Context**: Agent is fed rich prompt containing Zapier's cultural pillars:
  - Company Values (e.g., "growth mindset")
  - Meeting Norms (specific expectations)
  - Frameworks (e.g., "The Five Dysfunctions of a Team," demanding and supportive balance)
  - Impact Behaviors (expectations for employees)
- **Generate Personalized Feedback**: For each participant, AI analyzes their contributions against the cultural context
- **Deliver via Slack**: Feedback sent as DM, clearly stated as AI-generated, focuses on 1-2 growth opportunities and 1-2 actionable changes

**Iteration**: Initially feedback was too soft. Cortney iterated on instructions to strike a better balance between demanding and supportive. Result was more direct coaching like "Address misalignment more directly" or "Challenge the decision-making speed."

### Workflow 3: Stress-Testing Proposals with a Custom "Exec Prop" GPT

**Problem**: Cortney was the go-to person for pre-reviewing proposals before they reached the executive team, creating a bottleneck.

**Solution**: Custom GPT in ChatGPT that acts as a digital clone of the executive thought process.

**Knowledge Base includes**:
- Company strategy memos and revenue roadmap
- Examples of well-written proposals ("tee-ups")
- Team norms and decision-making processes
- "Managing Up to Wade" (CEO) document explaining his communication style and preferences

**Process**:
- Employee uploads draft document with prompt like "give feedback on a tee-up doc"
- GPT analyzes against entire knowledge base
- Structured output: summary of strengths/weaknesses, specific strengthening advice (e.g., "surface trade-offs more clearly"), example rewrite, and a "bold coaching question"

**Results**: 278+ employees have used it. Documents reaching the executive team are clearer, more aligned, and lead to faster decisions. In some cases, the document becomes clear enough that the meeting can be skipped entirely.

### Workflow 4: Building a Centralized Strategy Companion with NotebookLM

**Problem**: Company strategy is contained in dense documents or scattered across All-Hands presentations, making it difficult for employees to connect their work to the big picture.

**Solution**: Google NotebookLM as centralized, interactive strategy companion.

**Process**:
- **Aggregate All Sources**: Uploaded dozens of key strategic documents — top-level strategy doc, All-Hands transcripts, every organization's strategic action plan
- **Ask Questions in Natural Language**: Employees go to one central place and ask questions directly (e.g., "As an executive assistant, how can I contribute to Zapier's 2026 strategy?")
- **Get Contextual Answers**: Tool synthesizes answers based on source materials, pointing to specific documents
- **Explore Multimodal Content**: NotebookLM can generate AI podcasts summarizing strategy or interactive quizzes

Empowers every employee to understand how their individual role contributes to broader company goals, turning strategy from a top-down mandate into a resource everyone can own and interact with.

### Key Themes

The EA role is shifting from tactical support to strategic partner. By using AI, Cortney isn't just making her own job easier — she's building scalable systems that make the entire organization smarter, more aligned, and more effective. Her advice for getting started: find a repetitive task you do every week, and spend that time automating it instead.
