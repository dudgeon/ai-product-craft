---
title: "Brian Greenbaum's 3-Step Playbook for Driving Company-Wide AI Adoption"
created: 2026-02-15
updated: 2026-02-16
template: templates/source.md
template_version: 3
tags: [source, ai-pm, claude-added]
status: unread
source_type: podcast
source_url: "https://www.chatprd.ai/how-i-ai/3-step-playbook-for-ai-adoption"
archive_url: ""
author: "Brian Greenbaum"
host: "Claire Vo"
published: 2025-12-22
discovered: 2026-02-15
summary: "Brian Greenbaum (product designer at Pendo) shares a 3-step playbook for driving company-wide AI adoption: (1) start with a personal experience worth sharing and pitch leadership with a clear business case, (2) build a structured program with bi-weekly hands-on sessions plus an async Slack channel, and (3) measure sentiment via surveys and create a 'golden path' with an AI Knowledge Center of approved tools, data guidelines, and security status. The initiative led to Brian building an MCP server prototype connecting to Pendo's APIs that caught the CTO's attention and influenced the product roadmap."
domain: professional-development
project: ai-pm
# taxonomy_inference: ai-adoption (org-change, team-adoption, change-management)
# provenance: bulk-added by Claude from podcast-episode-compilation.md (2026-02-15)
# rescrape_needed: false — full article scraped from ChatPRD 2026-02-16
---

# Brian Greenbaum's 3-Step Playbook for Driving Company-Wide AI Adoption

**By**: Brian Greenbaum
**Host**: Claire Vo
**Source**: [How I AI (ChatPRD)](https://www.chatprd.ai/how-i-ai/3-step-playbook-for-ai-adoption)
**Type**: podcast

## Summary

Brian Greenbaum, a product designer at Pendo, shares how he built a step-by-step program to drive AI adoption across his product and design teams. It started with a personal epiphany on paternity leave when he used Cursor to build a working music app prototype in hours despite not being a developer. He pitched leadership with a dual business case (internal efficiency + external positioning), got buy-in from the CPO, and structured a program combining bi-weekly hands-on "Product AI" sessions with a public Slack channel for continuous sharing. His kickoff workshop had everyone use the same bolt.new prompt, revealing that identical prompts produce wildly different outputs — a teachable moment about iteration. To measure impact, his team surveyed sentiment before and after the quarter, seeing significant improvements in awareness of policies and available tools. He created an AI Knowledge Center with approved tools, data guidelines, and security status to replace shadow AI usage with sanctioned experimentation. The initiative culminated in Brian building a prototype MCP server connecting to Pendo's public APIs, generating interactive dashboards via natural language in Claude — a demo that caught the CTO's attention and directly influenced the product roadmap.

## Key Ideas Extracted

- **Personal experience as the catalyst**: Brian's paternity leave coding with Cursor was the credible, personal story that made his pitch to leadership compelling — you need a real experience worth sharing, not just theory
- **Dual business case framing**: Pitched AI adoption as both internal efficiency ("get more done in fewer hours") and external positioning (better serve customers going through AI transformation)
- **Hands-on workshops beat presentations**: Had everyone use the same prompt in bolt.new live — the surprise of wildly different outputs from identical prompts became a teachable moment about iteration and experimentation
- **"Radical many-to-many sharing"**: A public Slack channel for ongoing async conversation keeps momentum between scheduled sessions and creates a culture of visible experimentation
- **Survey-driven measurement**: Baseline and end-of-quarter surveys tracking sentiment, policy awareness, and tool familiarity showed concrete improvements and justified continued investment
- **AI Knowledge Center as "golden path"**: An alphabetized table of approved tools with data-sharing guidelines, security status, and a request process replaced confusion and shadow AI with sanctioned experimentation
- **Prototype as proof point**: Brian's MCP server connecting to Pendo's APIs demonstrated practical value that caught the CTO's attention and influenced the roadmap — showing, not telling
- **Three-part playbook**: (1) Start with personal experience + pitch leadership, (2) Structure regular hands-on sessions + async discussion, (3) Create clear guidelines with measurable outcomes

## Notes

This episode focuses less on specific AI workflows and more on organizational change management for AI adoption. The playbook is broadly applicable to any team or company trying to move from ad-hoc AI usage to a structured program. The MCP server prototype detail is particularly interesting — a product designer building an MCP server connecting to their company's APIs is a concrete example of how AI tools lower the bar for technical prototyping.

## Raw Content

Most How I AI episodes focus on specific workflows for building things. But a question constantly asked is: "How do I get my whole team to actually use this stuff?"

Brian Greenbaum, a product designer at Pendo, figured this out. He built a step-by-step program that got his product and design teams genuinely excited about AI.

### Workflow 1: Starting the Initiative

**Step 1: Have a Personal Experience Worth Sharing**

On paternity leave, Brian started playing with Cursor, an AI code editor. He had an idea for a music app — scan a QR code on a physical card to play an album on Spotify, like a modern record player. He's not a developer, but within a couple hours he had a working prototype — creating QR codes, PDFs, doing all sorts of things.

At Pendo, Brian works on analytics features where creating realistic data-driven prototypes in Figma is a constant challenge. He realized he could use tools like Cursor to build high-fidelity, code-based prototypes that communicate ideas far better than static mockups.

**Step 2: Make the Case to Leadership**

While still on leave, Brian drafted a Slack message to his manager, their manager, the CPO, and other AI enthusiasts. He framed it with a clear business case:
- **Internal efficiency**: The product team could leverage AI tools to get more done in fewer hours, improve decision making, and communicate ideas more effectively
- **External positioning**: By becoming proficient in AI, Pendo could better serve customers going through similar transformations

The CPO immediately asked him to present at the next all-hands. He had the buy-in to start a formal initiative.

### Workflow 2: Building the Program

**Step 1: Mix Scheduled Sessions with Ongoing Conversation**

The biggest barrier to AI adoption is time. Everyone knows it's important, but they're too busy to figure it out. Brian's solution: create both dedicated calendar time and a space for continuous learning.
- **Bi-weekly "Product AI" sessions**: Interactive meetings designed to get people's hands dirty, not just listen to presentations
- **Public Slack channel**: A hub for sharing articles, experiments, and questions — what Brian calls "radical many-to-many sharing"

**Step 2: Make Sessions Hands-On**

For his kickoff, Brian had everyone actually use AI, live. He designed a simple exercise using bolt.new:
1. **Same prompt, different results**: Everyone pasted the same prompt to create a to-do app. The eye-opener? Even with identical prompts, the AI generated wildly different apps. Some had errors — which became a teachable moment about iteration.
2. **Creative exploration**: Brian encouraged people to "go wild" with modifiers like "add a retro 8-bit pixel art theme" or "make it look like MySpace from 2007." People laughed, experimented, and saw the creative potential.

This hands-on approach made AI feel accessible. The Slack channel kept the conversation going after meetings ended. They even saw designers using Midjourney to create animated UI characters — something too time-consuming before.

### Workflow 3: Measuring and Scaling

**Step 1: Track Sentiment**

As part of a company OKR to improve AI adoption, Brian's group sent out a baseline survey asking about:
- Personal sentiment toward AI's impact
- Familiarity with company AI policies
- Awareness of which tools were available

They ran the survey at the start and end of the quarter. After implementing their programs, they saw significant improvements across all metrics — especially awareness of policies and available tools.

**Step 2: Create Clear Guidelines**

The survey revealed a big gap: people were using personal ChatGPT accounts and didn't know what data was safe to use or which tools were approved. Brian's team worked with legal, security, IT, and finance to create an AI Knowledge Center that included:
- An alphabetized table of approved AI tools
- Clear data-sharing guidelines for each (e.g., "Internal Data Only," "No PII")
- Security and legal status
- A process for requesting access or new tool evaluations

This replaced confusion with clarity. People could experiment safely instead of operating in the shadows.

### The Result

Brian used his new skills to build a prototype MCP server connecting to Pendo's public APIs. He recorded a demo showing how he could use natural language in Claude to generate interactive dashboards of product usage data. This caught the CTO's attention and directly influenced Pendo's roadmap, accelerating development of internal AI agents.

### The Playbook

Brian's approach comes down to three things:
1. Start with a personal experience that shows clear value, then make the case to leadership
2. Structure a program with regular hands-on sessions plus ongoing async discussion
3. Create a "golden path" with clear guidelines, approved tools, and measurable outcomes
