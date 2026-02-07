---
created: 2026-02-06
updated: 2026-02-07
template: templates/source.md
template_version: 2
tags: [source, ai-pm-craft, operations, agent-ops]
status: unread
source_type: article
source_url: "https://www.firstround.com/ai/brex"
archive_url: "domains/professional-development/ai-pm-craft/sources/2026-02-06-brex-agent-human-ops.md"
author: "James Reggio, Camilla Matias (First Round)"
published: 2025-09-25
discovered: 2026-02-06
summary: "Brex built a three-tier ops model (L1 fully automated BPO replacement, L2 agent+people management, L3 strategic experts) on an internal Retool-based agent platform. 50%+ CS cases resolved by AI; 15 roles migrated from L1→L2. Key insights: set 100% automation as target not 40%, AI beats humans at subjective judgment tasks (adverse media, email personalization), and hire for AI-leveraging problem-solving not domain expertise."
domain: professional-development
project: ai-pm-craft
---

# Agent + Human Ops: How AI is Changing Roles and Workflows at Brex

**By**: James Reggio (CTO), Camilla Matias (COO) — via First Round
**Source**: [First Round](https://www.firstround.com/ai/brex)
**Type**: article

## Summary

*Fill after reading. 2-3 sentences: what is this about, what's the core argument or insight?*

## Key Ideas Extracted

*Fill during processing. Each idea links to a knowledge entry.*

## Notes

*Your annotations, reactions, questions, disagreements. Written during or after reading.*

## Raw Content

Brex CTO James Reggio spends a lot of time thinking about how AI can make Brex disappear. "Nobody wakes up and says 'I can't wait to spend time in Brex,'" he says.

"We believe the best user interface is just the card that lets you swipe and go. Most of our investments on the product AI side are oriented around the thinking of eliminating Brex from your overall experience. The best AI is the AI that you don't notice because it's taken work away."

Camilla Matias, Brex's COO, shares this thinking, except she's looking inward at the company's operations — using AI to reduce the toil of the most manual, prescriptive work.

"If I was starting the company today in this new AI era, I'd build operations completely different," says Matias. "We can't just use ChatGPT. The roles must be different. We're changing what we expect from people."

### Three AI Pillars + Hidden Fourth

1. Product AI (customer-facing features)
2. Operational AI (internal processes)
3. Corporate AI (employee day-to-day tools)
4. AI Platform (unified infrastructure serving all three)

### Internal Agent Platform Built in Retool

- Prompt management system
- Multi-model testing
- Evaluation frameworks
- API integrations for automated workflows
- Treated as external product with 25-person systems engineering team
- "We treat it like an external product, and in some ways, it is"

Product loop: internal and external features improve simultaneously. "The functionality of our internal MCP has rapidly evolved because it's the same as our external MCP."

### Legal/Procurement Innovation

- Approval tracks based on data lifecycle, not vendor identity
- Pre-approved sub-categories with defined controls
- Employees self-provision via Slack (/c1 command)
- Eliminates case-by-case legal reviews
- "Philosophically, we don't want to pick winners among tools. But we have the data to show which ones our employees want."

### Three-Level Operations Model

**L1:** Fully automated, process-driven work (BPO replacement). "Anywhere you have a BPO, you usually have a well-defined SOP and work that's parceled up effectively to be handled by an LLM." Over 50% of cases resolved by chatbot as first touchpoint. 15+ CS roles migrated to L2.

**L2:** Agent management + complex cases requiring judgment. Changed from people management to agent+people management. "L2s used to manage people. Now my expectation is that they're managing agents as well." New skills: prompt engineering, workflow analysis, human-in-the-loop QA design.

**L3:** Strategic experts with deep industry knowledge. Fraud prevention, credit strategy. LLM helps parse patterns and aggregate data, but humans set strategy.

### AI Literacy Framework

- Mandatory course for all operations team
- Four proficiency levels: User, Advocate, Builder, Native
- Bottom quartile paired with high performers for mentorship
- Office hours with systems engineering team

### Hiring for Generalists

- Prioritize AI-leveraging problem-solving over domain expertise
- Case studies require demonstrating AI tool usage
- Review prompts and iteration process, not just outputs
- "We request to see how they're prompting and see how they did the work using AI. The outputs don't really matter."

### Rebuilding Workflows Around AI Strengths

**Automation Criteria:**
1. Time consumption (high-volume tasks)
2. AI's advantage over humans (measurable improvement)
3. Implementation speed (quick wins)

**100% Automation Mindset:** "When you set the goal at 100% automation as opposed to 40% automation, you end up making investments in AI tooling and infrastructure that you wouldn't otherwise."

**Unexpected AI Strengths:**
- Subjective judgment (adverse media recognition: 85% → 88%)
- Email personalization (better response rates than human-modified templates)
- Complex rule understanding (disputes: 3 hours → 3 seconds, better quality)
- Clearly-laid out steps (KYC: 8-10 of 14 steps automated with high confidence)

### Impact

- 50%+ customer support cases resolved by AI first touchpoint
- 15 CS roles migrated from L1 to L2
- 5x-10x efficiency gains projected
- Removes engineering bottleneck for new processes/markets
