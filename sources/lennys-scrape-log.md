---
created: 2026-02-17
updated: 2026-02-17
tags: [scrape-log, lennys-newsletter, ai-pm]
status: active
domain: professional-development
project: ai-pm
scrape_range: "2023-02-05 to 2026-02-15"
scrape_sections: "lennysnewsletter.com — AI-relevant newsletters and podcast episodes only"
scraped_by: claude
---

# Lenny's Newsletter — Scrape Log

Tracks every article/episode considered from lennysnewsletter.com, with scrape decisions and links to source files. Used to avoid re-processing on future runs.

**Scrape run**: 2026-02-19 (added 2 articles: Caitlin Sullivan guest post 2/18, Boris Cherny podcast 2/19)
**Previous run**: 2026-02-15 (selective — AI-relevant content only, no systematic full-catalog scan)
**Next run**: Check lennysnewsletter.com for new AI-focused content since Feb 19, 2026. Use skip criteria below to filter.

---

## Publication Overview

Lenny's Newsletter (lennysnewsletter.com) is Lenny Rachitsky's weekly PM/startup publication. Two content formats:

- **Newsletter issues**: Lenny's own writing on PM topics, plus frequent guest posts
- **Lenny's Podcast**: Long-form interviews with founders, PMs, and leaders (published as newsletter posts)

The publication covers the full breadth of product management — only a subset is relevant to ai-pm-craft. Scraping was **selective**: focused on AI workflow content, AI-PM disruption essays, and interviews with practitioners demonstrating AI-native approaches.

---

## Decision Key

| Decision | Meaning |
|---|---|
| `scrape` | Captured as ai-pm source |
| `skip` | Not captured — see reason |

---

## Skip Criteria

**Always scrape**:
- Lenny's own newsletter issues on AI's impact on PM roles
- Guest posts demonstrating AI workflows for PM/design/engineering
- Podcast episodes where the primary topic is AI tooling or AI-native work patterns
- Any content on AI-PM career disruption or skill shift

**Usually skip**:
- General PM strategy without AI angle (discovery, roadmapping frameworks, OKRs, etc.)
- Startup/GTM content without AI focus (pricing, growth loops, sales funnels)
- PM career advice without AI context (interviews, resumes, salary negotiation)
- Technical deep-dives aimed at engineers rather than PMs (unless AI-workflow relevant)
- Product metrics / analytics content without AI tooling angle
- Podcast episodes where guest's work is interesting but the conversation doesn't surface transferable AI practices
- Older content (pre-2023) — predates meaningful AI practice content

---

## Scraped Articles

### Podcast Episodes

| Date | Guest | Context | Source File |
|---|---|---|---|
| 2023-02-05 | Marily Nika | AI and product management (Meta Reality Labs; PhD ML) | [2023-02-05-marily-nika-ai-and-product-management.md](2023-02-05-marily-nika-ai-and-product-management.md) |
| 2024-09-08 | Tomer Cohen | LinkedIn transformation: AI-powered feed reinvention (CPO LinkedIn) | [2024-09-08-linkedin-transformation-tomer-cohen.md](2024-09-08-linkedin-transformation-tomer-cohen.md) |
| 2025-06-05 | Mike Krieger | Anthropic CPO on AI-native product philosophy (co-founder Instagram) | [2025-06-05-anthropic-cpo-mike-krieger.md](2025-06-05-anthropic-cpo-mike-krieger.md) |
| 2025-07-06 | Maor Shlomo | Base44: solo founder, AI app builder, $1M ARR in 3 weeks | [2025-07-06-base44-bootstrapped-startup-maor-shlomo.md](2025-07-06-base44-bootstrapped-startup-maor-shlomo.md) |
| 2025-09-07 | Oji & Ezinne Udezue | AI reshaping the product role (50+ yrs PM leadership) | [2025-09-07-ai-reshaping-product-role-udezue.md](2025-09-07-ai-reshaping-product-role-udezue.md) |
| 2025-12-04 | Tomer Cohen | LinkedIn replacing PMs with full-stack builders | [2025-12-04-linkedin-replacing-pms-full-stack-builders.md](2025-12-04-linkedin-replacing-pms-full-stack-builders.md) |
| 2025-12-14 | Alexander Embiricos | Humans as biggest bottleneck (Product Lead, Codex, OpenAI) | [2025-12-14-humans-biggest-bottleneck-alexander-embiricos.md](2025-12-14-humans-biggest-bottleneck-alexander-embiricos.md) |
| 2025-12-18 | Elena Verna | AI growth playbook 2026 (Head of Growth, Lovable) | [2025-12-18-ai-growth-playbook-2026-elena-verna-lovable.md](2025-12-18-ai-growth-playbook-2026-elena-verna-lovable.md) |

### Newsletter Issues & Guest Posts

| Date | Author | Title/Topic | Source File |
|---|---|---|---|
| 2024-07-09 | Mike Taylor | How close is AI to replacing PMs? (guest post) | [2024-07-09-how-close-ai-replacing-product-managers.md](2024-07-09-how-close-ai-replacing-product-managers.md) |
| 2024-08-13 | Marily Nika | Summary: AI and PM (written summary of Feb 2023 episode) | [2024-08-13-summary-ai-product-management-marily-nika.md](2024-08-13-summary-ai-product-management-marily-nika.md) |
| 2025-01-07 | Colin Matthews | Guide to AI prototyping for PMs (guest post) | [2025-01-07-guide-ai-prototyping-product-managers.md](2025-01-07-guide-ai-prototyping-product-managers.md) |
| 2025-05-13 | Lenny Rachitsky | State of the PM job market 2025 | [2025-05-13-state-product-job-market-2025.md](2025-05-13-state-product-job-market-2025.md) |
| 2025-06-10 | Colin Matthews | Get your entire team prototyping with AI (guest post) | [2025-06-10-get-entire-team-prototyping-ai.md](2025-06-10-get-entire-team-prototyping-ai.md) |
| 2025-07-08 | Lenny Rachitsky | What people are vibe coding (crowdsourced) | [2025-07-08-what-people-are-vibe-coding.md](2025-07-08-what-people-are-vibe-coding.md) |
| 2026-02-06 | Tal Raviv & Aman Khan | Build AI product sense (guest post) | [2026-02-06-build-ai-product-sense.md](2026-02-06-build-ai-product-sense.md) |
| 2026-02-08 | Lenny Rachitsky | How AI will impact product management | [2026-02-08-how-ai-will-impact-product-management.md](2026-02-08-how-ai-will-impact-product-management.md) |
| 2026-02-08 | Lenny Rachitsky (with Lazar Jovanovic) | Getting paid to vibe code | [2026-02-08-vibe-coding-new-ai-job.md](2026-02-08-vibe-coding-new-ai-job.md) |
| 2026-02-08 | Tal Raviv | Make PM fun again with AI agents (guest post) | [2026-02-08-make-pm-fun-again-ai-agents.md](2026-02-08-make-pm-fun-again-ai-agents.md) |
| 2026-02-08 | Marily Nika | PM AI toolkit demo (How I AI / Lenny's crosspost) | [2026-02-08-marily-nika-pm-ai-toolkit.md](2026-02-08-marily-nika-pm-ai-toolkit.md) |
| 2026-02-10 | Marily Nika | Building AI product sense, part 2 (guest post) | [2026-02-10-building-ai-product-sense-part-2-marily-nika.md](2026-02-10-building-ai-product-sense-part-2-marily-nika.md) |
| 2026-02-13 | Lenny Rachitsky | Everyone should use Claude Code more | [2026-02-13-everyone-should-use-claude-code-more.md](2026-02-13-everyone-should-use-claude-code-more.md) |
| 2026-02-18 | Caitlin Sullivan | How to do AI analysis you can actually trust (guest post) | [2026-02-18-ai-analysis-you-can-actually-trust.md](2026-02-18-ai-analysis-you-can-actually-trust.md) |
| 2026-02-19 | Boris Cherny | Head of Claude Code: What happens after coding is solved (podcast) | [2026-02-19-head-of-claude-code-boris-cherny.md](2026-02-19-head-of-claude-code-boris-cherny.md) |

---

## Inferred Skipped Content

Lenny's Newsletter publishes weekly and covers the full range of PM topics. Only AI-relevant content was scraped. The following categories were not captured:

### Systematically Skipped (no source files created)

| Category | Examples | Reason |
|---|---|---|
| General PM frameworks | Discovery, roadmapping, prioritization, OKRs | Not AI-specific |
| Startup strategy | GTM, pricing, growth loops, PLG | Not AI-specific |
| PM career advice | Interview prep, salary, career progression | Not AI-specific |
| User research / design | UX research methods, design systems | Not AI-angle |
| Fundraising / VC | Pitch decks, term sheets, investor relations | Not AI-specific |
| Data & analytics | Metrics, A/B testing, analytics frameworks | Not AI-specific |
| Pre-2023 back-catalog | Entire archive before ~Feb 2023 | Predates AI practice content |

### Specific Skipped Articles (inferred from context)

These represent known or likely Lenny's content that was present but not relevant enough to capture:

| Date | Topic | Inferred reason for skip |
|---|---|---|
| 2025-ongoing | Lenny's weekly "Ask Lenny" posts | Q&A format, too scattered for extraction |
| 2025-ongoing | Non-AI podcast episodes | Guests with no AI workflow content (e.g., hiring, growth, GTM-only) |
| 2025-05-13 | State of product job market | Scraped for AI angle; most of it is general PM hiring data |
| 2023–2024 back-catalog | Pre-AI-wave PM content | Not scraped; may contain early AI takes but low signal/noise |

---

## Stats

- **Podcast episodes scraped**: 9
- **Newsletter issues / guest posts scraped**: 14
- **Total scraped**: 23
- **Coverage**: Highly selective — only AI-relevant content from 2023–present. Lenny's publishes 50+ issues/year; the vast majority were skipped.
- **Catalog note**: No systematic page-by-page scan was done. Coverage reflects articles surfaced through curation and direct links, not exhaustive crawl. Future runs should search lennysnewsletter.com for AI-tagged content.
