---
created: 2026-02-07
updated: 2026-02-07
template: templates/source.md
template_version: 2
tags: [source, ai-pm-craft]
status: unread
source_type: article
source_url: "https://www.chatprd.ai/how-i-ai/zapier-workflows-for-crm-automation-meeting-prep"
archive_url: "domains/professional-development/ai-pm-craft/sources/2026-02-07-zapier-workflows-crm-automation-meeting-prep.md"
author: "Claire Vo (Reid Robinson)"
published: 2026-02-04
discovered: 2026-02-07
summary: "Zapier PM Reid Robinson demos three practical AI workflows: MCP-powered CRM automation (15min task→copy-paste), always-on meeting prep assistant (deterministic Zap pulling Databricks+calendar data), and a self-improving customer feedback loop (closed tickets→FAQ extraction→human review→chatbot enrichment). Key framework: combine agentic (chat-based MCP) with deterministic (scheduled Zap) approaches."
domain: professional-development
project: ai-pm-craft
---

# Reid Robinson's Zapier Workflows for CRM Automation, Meeting Prep, and Feedback Loops

**By**: Claire Vo (interviewing Reid Robinson, PM on AI at Zapier)
**Source**: [ChatPRD How I AI](https://www.chatprd.ai/how-i-ai/zapier-workflows-for-crm-automation-meeting-prep)
**Type**: article

## Summary

*Fill after reading.*

## Key Ideas Extracted

*Fill during processing.*

## Notes

*Your annotations, reactions, questions, disagreements.*

## Raw Content

Reid Robinson, a product manager on AI at Zapier, demonstrates practical AI workflows combining agentic and deterministic approaches to automate CRM updates, meeting prep, and customer feedback loops.

### Workflow 1: Automating CRM Updates with Claude and Zapier MCPs

**Setup:**
- Uses Zapier MCP server to create custom toolset for Claude
- Toolset includes: Coda, Google Calendar, Slack, Evernote, Glean
- Claude Projects provides instructions on tool usage order

**The "Secret Sauce":**
> Reid uses Claude Projects to provide *instructions* on tool usage rather than just context. This guides the model to consistent and accurate outcomes by specifying the exact sequence of operations.

**Example workflow:**
1. Search Coda document for existing contact record
2. If not found, use internal lookup tool
3. Create new entry in Coda based on meeting notes
4. Populate fields according to specific definitions

**Result:** 15-minute manual task becomes simple copy-paste

### Workflow 2: The "Always-On" Meeting Prep Assistant

**Deterministic Zapier workflow that:**
1. Triggers on new customer interview in calendar
2. Fetches data:
   - Queries Databricks for company usage, sales history
   - Converts HTML output to processable format
   - Uses Google Gemini (excellent for file processing) to summarize
3. Appends summary to Coda page for the meeting

**Key insight:** Gemini models are exceptionally good at handling files (PDFs, audio, video, HTML)

### Workflow 3: Building a Self-Improving Customer Feedback System

**The virtuous cycle:**
1. **Analysis Zap** triggers on closed support ticket/chatbot conversation
   - Identifies core question/issue
   - Extracts solution provided
2. **Human-in-the-loop Review**
   - Checks if Q&A exists in knowledge base (Zapier Table)
   - Proposes new FAQ entry if missing
   - Sends to human for review/approval
3. **Closing the loop**
   - Approved FAQs added to Zapier Table
   - Table powers internal chatbot for sales/PMM teams
   - Chatbot gets smarter automatically every day

### Personal Use Cases

**Family Calendar Assistant:**
- Take photo of physical calendar → send to Claude with Project instructions → Zapier MCP updates Google Calendar → auto-blocks driving time

**Interview Prep as Love Language:**
- Used Notebook AI to create personalized interview prep podcasts from career page, job description, competitor articles

**Making Music with Kids:**
- Claude + Suno to create songs with 4-year-old son; teaches specific prompting

### Key Concepts & Frameworks

**MCPs = "App integrations for your AI tools"** — Model Context Protocols give AI access to knowledge and actions locked in thousands of apps

**The Framework Question:** "If you could run ChatGPT in your sleep, what would you do?"

**Meeting Users Where They Are:** Combine agentic workflows (in-the-moment, chat-based with MCPs) with deterministic workflows (asynchronous, predictable Zaps)

**Perfect Team Framework:** "What would your perfect team with infinite time do?" Example: Analyze every customer interaction, identify knowledge gaps, update help docs immediately

### Technical Implementation Notes

- Zapier MCP bundles actions from 8,000+ apps into single secure connection
- Claude Projects: use for instructions, not just context — models get confused with similar action names
- Gemini: exceptionally good for file processing; Claude: best for following complex instructions with tools
- Human-in-the-loop crucial for maintaining quality in automated systems

### Actionable Takeaways

1. Start with one tedious task you hate (like CRM updates)
2. Think about what your AI could do while you sleep
3. Combine agentic (chat-based) and deterministic (Zap-based) approaches
4. Use Claude Projects for reliable tool usage instructions
5. Build human-in-the-loop review for quality control
6. Create virtuous cycles that compound value over time
