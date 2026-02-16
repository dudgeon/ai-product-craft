---
title: "How Suzy's CEO Turns 25,000 Hours of Sales Calls into Automated Marketing and Coaching with One Zapier Workflow"
created: 2026-02-15
updated: 2026-02-16
template: templates/source.md
template_version: 3
tags: [source, ai-pm, claude-added]
status: unread
source_type: podcast
source_url: "https://www.chatprd.ai/how-i-ai/sales-calls-into-automated-marketing-and-coaching-with-ai-zapier"
archive_url: ""
author: "Matt Britton"
host: "Claire Vo"
published: 2025-11-10
discovered: 2026-02-15
summary: "Matt Britton (founder/CEO, Suzy — consumer insights platform) on How I AI. One mega-workflow in Zapier that takes a single Gong call transcript and extracts maximum value across the entire GTM org: (1) Trigger — hacked Gong data access via Browse AI web scraping (identified URL pattern with call_id, triggered on new calls, Browse AI scrapes full transcript); (2) Data prep — 2-minute delay buffer, HTML stripping via Zapier Formatter, Google Sheets lookup to enrich with brand name, salesperson, manager, Slack ID; (3) Core analysis — GPT-4 Turbo generates structured summary, sentiment score (1-10, predictive of churn), opportunities, and action items from single prompt; (4) Internal distribution — posts to general Slack channel + auto-routes low-sentiment scores (<7) to 'Churn Early Warning System' channel; (5) AI coaching — separate LLM step analyzes employee performance, sends personalized feedback, logs to central dataset for manager trend tracking; (6) Marketing engine — extracts customer language as Google Ads keywords (closed-loop from happy customers to acquisition), auto-generates anonymized SEO blog posts with headline/graphic/CTA scheduled 21 days out (10,000+ posts generated); (7) Follow-up email writer — drafts personalized follow-up with human-in-the-loop review. Core insight: your most valuable data is already being created — 25,000 hours of recorded calls are a treasure trove. Non-engineer CEO built the entire system."
domain: professional-development
project: ai-pm
# taxonomy_inference: product-lifecycle/measure (customer-feedback-collection); product-lifecycle/release (launch-marketing-enablement); horizontal/agents (Zapier-workflows)
# provenance: bulk-added by Claude from podcast-episode-compilation.md (2026-02-15)
# rescrape_needed: false — re-scraped from ChatPRD 2026-02-16
---

# How Suzy's CEO Turns 25,000 Hours of Sales Calls into Automated Marketing and Coaching with One Zapier Workflow

**By**: Matt Britton
**Host**: Claire Vo
**Source**: [How I AI (ChatPRD)](https://www.chatprd.ai/how-i-ai/sales-calls-into-automated-marketing-and-coaching-with-ai-zapier)
**Type**: podcast

## Summary

How I AI episode with Matt Britton, founder and CEO of Suzy (consumer insights platform). One mega-workflow in Zapier that transforms a single Gong call transcript into company-wide intelligence across seven steps: (1) Trigger — hacked Gong data access using Browse AI web scraping when direct integration didn't exist (identified URL pattern with unique call_id, set Zap to trigger on new calls, Browse AI builds full URL and scrapes raw transcript); (2) Data prep and enrichment — 2-minute delay buffer to prevent errors, Zapier Formatter strips HTML tags, Google Sheets lookup enriches with brand name, salesperson name, manager, and Slack user ID; (3) Core analysis — GPT-4 Turbo prompt generates structured summary, sentiment score (1-10 scale, proven churn predictor), customer frustrations, opportunities, and next steps from a single prompt; (4) Internal distribution — every call summary posts to main Slack channel for company-wide visibility, sentiment scores below threshold auto-route to dedicated "Churn Early Warning System" channel; (5) AI-powered coaching — separate LLM step analyzes employee performance on the call, sends personalized feedback (what went well, what to improve) directly to the individual, logs to central dataset for manager trend tracking and objective performance reviews; (6) Marketing engine — extracts customer language as Google Ads keywords (closed-loop: happy customer language attracts similar prospects), auto-generates fully anonymized SEO-optimized blog posts with PII redaction, headline, graphic, and CTA, scheduled 21 days out (10,000+ blog posts generated from real customer challenges); (7) Follow-up email writer — drafts personalized follow-up email from call context, sends to employee for human-in-the-loop review before sending.

## Key Ideas Extracted

- **One asset, seven outputs**: A single call transcript generates summaries, churn alerts, coaching feedback, performance data, Google Ads keywords, blog content, and follow-up emails — maximum value extraction from existing data
- **Browse AI as integration hack**: When direct API triggers don't exist, use web scraping tools to build the data pipeline — identify URL patterns, trigger on events, scrape the page content
- **Sentiment score as churn predictor**: AI-generated 1-10 sentiment scores from call transcripts reliably predict churn risk — auto-routing low scores to a dedicated alert channel enables proactive intervention
- **AI coaching with centralized performance tracking**: Personalized feedback sent directly to employees after each call + logged to central dataset — creates objective, data-driven performance reviews based on actual customer interactions
- **Closed-loop customer language → ad keywords**: Extract the exact words customers use to describe their problems, feed directly into Google Ads — acquisition messaging mirrors the language of successful customers
- **Automated content generation at massive scale**: Anonymize transcripts (redact PII) → LLM writes SEO blog posts → schedule 21 days out → 10,000+ posts from real customer challenges — continuous content pipeline from existing conversations
- **2-minute delay buffer for complex Zaps**: Add a delay after triggers to ensure all data is fully received before processing — simple trick that prevents cascading errors in multi-step automations
- **Non-engineer CEO built the system**: Matt isn't an engineer but built the entire mega-workflow himself — demonstrates that leaders who get hands-on with AI tools have a massive advantage

## Notes

- Published Nov 10, 2025 on How I AI (ChatPRD). ~9 min read.
- Sponsors: Brex, Zapier
- Matt Britton background: Founder/CEO of Suzy (consumer insights platform); sold first Facebook ads, bought early Google keywords; author of "Generation AI"
- Tools: Zapier (orchestration), Gong (call recording), Browse AI (web scraping), ChatGPT/GPT-4 Turbo (analysis), Google Sheets (data enrichment), Slack (distribution), Google Ads (keywords)
- Scale: 25,000 hours of recorded calls; 10,000+ auto-generated blog posts
- Key concept: "Super individual contributor" — proactive problem-solvers who build AI solutions themselves
- Three companion workflow guides published Jan 8, 2026
- Cross-references: Zapier mega-workflows, Gong integration, churn prediction, AI coaching, content-from-calls pipeline

## Raw Content

*Re-scraped from ChatPRD 2026-02-16. Full article content captured in Summary and Key Ideas above.*
