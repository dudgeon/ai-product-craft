---
created: 2026-02-17
updated: 2026-02-20
tags: [scrape-log, every-to, ai-pm]
status: active
domain: professional-development
project: ai-pm
scrape_range: "2025-09-02 to 2026-02-20"
scrape_pages: "every.to/newsletter pages 1–6"
scraped_by: claude
---

# Every.to Newsletter — Scrape Log

Tracks every article considered from every.to/newsletter, with scrape decisions and links to source files. Used to avoid re-processing on future runs.

**Scrape run**: 2026-02-20 (added 1 article: Katie Parrott board games Feb 19)
**Previous run**: 2026-02-17 (pages 1–6, covering Sep 2, 2025 – Feb 17, 2026)
**Next run**: Start from Feb 20, 2026 and check for new articles above last scraped date.

---

## Column Guide

Every.to uses URL-prefix "columns" that predict article type:

| Column prefix | Type | Default decision |
|---|---|---|
| `source-code/` | Technical/engineering how-tos | Usually SCRAPE |
| `chain-of-thought/` | Dan Shipper essays | Case-by-case |
| `context-window/` | Every Staff newsletter digests | Usually SKIP |
| `vibe-check/` | Tool/model reviews | Usually SKIP |
| `podcast/` | Interviews | Usually SCRAPE |
| `on-every/` | Company announcements, events, product launches | Always SKIP |
| `also-true-for-humans/` | AI & human behavior | Usually SCRAPE |
| `thesis/` | Strategic essays | Usually SCRAPE |
| `working-overtime/` | Personal productivity stories | Case-by-case |
| `playtesting/` | Game AI (Every's Good Start Labs column) | Usually SKIP |
| `learning-curve/` | Learning with AI | Usually SCRAPE |
| `p/` | General articles | Case-by-case |

---

## Decision Key

| Decision | Meaning |
|---|---|
| `scrape` | Captured as ai-pm source |
| `skip` | Not captured — see reason |
| `pending` | Queued for scraping on this run |

---

## Articles

### Page 1 — Feb 17 to Jan 23, 2026

| Date | Title | Author | URL | Decision | Reason / Source File |
|---|---|---|---|---|---|
| 2026-02-19 | What Board Games Taught Me About Working with AI | Katie Parrott | [link](https://every.to/working-overtime/what-board-games-taught-me-about-working-with-ai) | scrape | [2026-02-19-board-games-taught-me-working-with-ai.md](2026-02-19-board-games-taught-me-working-with-ai.md) |
| 2026-02-17 | Introducing Monologue for iOS | Naveen Naidu | [link](https://every.to/on-every/introducing-monologue-for-ios) | skip | Every product announcement |
| 2026-02-17 | How to Build Agent-native: Lessons From Four Apps | Katie Parrott | [link](https://every.to/source-code/how-to-build-agent-native-lessons-from-four-apps) | scrape | [2026-02-17-how-to-build-agent-native-lessons-from-four-apps.md](2026-02-17-how-to-build-agent-native-lessons-from-four-apps.md) |
| 2026-02-13 | AI as Fast as Your Train of Thought | Every Staff | [link](https://every.to/context-window/ai-as-fast-as-your-train-of-thought) | skip | Newsletter digest |
| 2026-02-13 | The Two-slice Team | Dan Shipper | [link](https://every.to/chain-of-thought/the-two-slice-team) | scrape | [2026-02-13-the-two-slice-team.md](2026-02-13-the-two-slice-team.md) |
| 2026-02-12 | How Claude Code Is Transforming Finance—Without Turning You Into a Coder | Brooker Belcourt | [link](https://every.to/p/how-claude-code-is-transforming-finance-without-turning-you-into-a-coder) | scrape | [2026-02-12-claude-code-transforming-finance.md](2026-02-12-claude-code-transforming-finance.md) |
| 2026-02-11 | Inside OpenAI's Agentic Browser, Atlas | Rhea Purohit (Ben Goodger, Darin Fisher) | [link](https://every.to/podcast/inside-openai-s-agentic-browser-atlas) | scrape | [2026-02-11-inside-openai-agentic-browser-atlas.md](2026-02-11-inside-openai-agentic-browser-atlas.md) |
| 2026-02-10 | Introducing Every Events | Natalia Quintero | [link](https://every.to/on-every/introducing-every-events) | skip | Every event announcement |
| 2026-02-09 | Compound Engineering: The Definitive Guide | Kieran Klaassen | [link](https://every.to/source-code/compound-engineering-the-definitive-guide) | scrape | [2026-02-09-compound-engineering-definitive-guide.md](2026-02-09-compound-engineering-definitive-guide.md) |
| 2026-02-06 | The Ur-model Cometh | Every Staff | [link](https://every.to/p/the-ur-model-cometh) | skip | Newsletter digest mentioning Every consulting |
| 2026-02-06 | What Is Taste, Really? | Jack Cheng | [link](https://every.to/p/what-is-taste-really) | skip | Creativity/taste essay, not ai-pm |
| 2026-02-05 | GPT-5.3 Codex vs. Opus 4.6: The Great Convergence | Vibe Check | [link](https://every.to/vibe-check/codex-vs-opus) | skip | Model comparison vibe check |
| 2026-02-05 | Vibe Check: Opus 4.6—The Best Coding Model We've Tested | Dan Shipper | [link](https://every.to/vibe-check/opus-4-6) | skip | Model vibe check |
| 2026-02-05 | Vibe Check: GPT-5.3 Codex—The 10x Engineer, Now More Fun at Parties | Every Staff | [link](https://every.to/vibe-check/gpt-5-3-codex) | skip | Model vibe check |
| 2026-02-04 | Every's Head of Consulting Just Automated Her Job | Tom Matsuda (Natalia Quintero) | [link](https://every.to/podcast/everys-head-of-consulting-just-automated-her-job) | scrape | [2026-02-04-everys-head-of-consulting-automated-her-job.md](2026-02-04-everys-head-of-consulting-automated-her-job.md) |
| 2026-02-03 | We Trained an AI on a Board Game. It Became a Better Customer Support Agent. | Alex Duffy | [link](https://every.to/playtesting/we-trained-an-ai-on-a-board-game-it-became-a-better-customer-support-agent-299b5938-09dd-4881-803f-aea21f0d461f) | scrape | [2026-02-03-board-game-training-customer-support-agent.md](2026-02-03-board-game-training-customer-support-agent.md) |
| 2026-02-03 | The Next Chapter of Every Consulting | Natalia Quintero | [link](https://every.to/on-every/the-next-chapter-of-every-consulting) | skip | Every business announcement |
| 2026-02-02 | Vibe Check: OpenAI's Codex App Gains Ground on Claude Code | Dan Shipper | [link](https://every.to/vibe-check/vibe-check-openai-s-codex-app-gains-ground-on-claude-code) | skip | Tool comparison vibe check |
| 2026-01-31 | Give Yourself a Promotion | Every Staff | [link](https://every.to/context-window/give-yourself-a-promotion) | skip | Newsletter digest |
| 2026-01-30 | Compound Engineering: How Every Codes With Agents | Dan Shipper | [link](https://every.to/source-code/compound-engineering-how-every-codes-with-agents-af3a1bae-cf9b-458e-8048-c6b4ba860e62) | scrape | [2026-01-30-compound-engineering-how-every-codes-with-agents.md](2026-01-30-compound-engineering-how-every-codes-with-agents.md) |
| 2026-01-29 | Teach Your AI to Think Like a Senior Engineer | Kieran Klaassen | [link](https://every.to/source-code/teach-your-ai-to-think-like-a-senior-engineer-789ba7ca-ca7c-45a1-91fa-4178f59f226f) | scrape | [2026-01-29-teach-your-ai-to-think-like-senior-engineer.md](2026-01-29-teach-your-ai-to-think-like-senior-engineer.md) — ⚠️ Duplicate URL slug of Nov 7 article |
| 2026-01-28 | Stop Coding and Start Planning | Kieran Klaassen | [link](https://every.to/source-code/stop-coding-and-start-planning-be0b4fd1-5898-4b09-bfda-0b00ea0004fd) | scrape | [2026-01-28-stop-coding-and-start-planning.md](2026-01-28-stop-coding-and-start-planning.md) — ⚠️ Duplicate URL slug of Nov 6 article |
| 2026-01-27 | My AI Had Already Fixed the Code Before I Saw It | Kieran Klaassen | [link](https://every.to/source-code/my-ai-had-already-fixed-the-code-before-i-saw-it-f4a29a07-ea95-409f-bcb2-487a970bed4a) | scrape | [2026-01-27-my-ai-had-already-fixed-the-code.md](2026-01-27-my-ai-had-already-fixed-the-code.md) |
| 2026-01-26 | How I Use Claude Code to Ship Like a Team of Five | Kieran Klaassen | [link](https://every.to/source-code/how-i-use-claude-code-to-ship-like-a-team-of-five-6f23f136-52ab-455f-a997-101c071613aa) | scrape | [2026-01-26-how-i-use-claude-code-ship-team-of-five.md](2026-01-26-how-i-use-claude-code-ship-team-of-five.md) |
| 2026-01-23 | The Vibe Coders' Guide to What's Next | Every Staff | [link](https://every.to/context-window/the-vibe-coders-guide-to-what-s-next) | skip | Newsletter digest |

### Page 2 — Jan 23 to Dec 19, 2025

| Date | Title | Author | URL | Decision | Reason / Source File |
|---|---|---|---|---|---|
| 2026-01-23 | I Stopped Reading Code. My Code Reviews Got Better. | Kieran Klaassen | [link](https://every.to/source-code/i-stopped-reading-code-my-code-reviews-got-better) | scrape | [2026-01-23-i-stopped-reading-code-reviews-got-better.md](2026-01-23-i-stopped-reading-code-reviews-got-better.md) |
| 2026-01-22 | What the Team Behind Cursor Knows About the Future of Code | Katie Parrott | [link](https://every.to/source-code/what-the-team-behind-cursor-knows-about-the-future-of-code) | scrape | [2026-01-22-cursor-team-future-of-code.md](2026-01-22-cursor-team-future-of-code.md) |
| 2026-01-21 | Opus 4.5 Changed How Andrew Wilkinson Works and Lives | Rhea Purohit (Andrew Wilkinson) | [link](https://every.to/podcast/opus-4-5-changed-how-andrew-wilkinson-works-and-lives) | scrape | [2026-01-21-andrew-wilkinson-opus-ai-changed-how-he-works.md](2026-01-21-andrew-wilkinson-opus-ai-changed-how-he-works.md) |
| 2026-01-20 | What AI Is Teaching Us About Management | Mike Taylor | [link](https://every.to/also-true-for-humans/what-ai-is-teaching-us-about-management) | scrape | [2026-01-20-what-ai-teaches-us-about-management.md](2026-01-20-what-ai-teaches-us-about-management.md) |
| 2026-01-18 | Claude Code Takes Pole Position | Every Staff | [link](https://every.to/context-window/claude-code-takes-pole-position) | skip | Newsletter digest |
| 2026-01-16 | OpenAI Has Some Catching Up to Do | Dan Shipper | [link](https://every.to/chain-of-thought/openai-has-some-catching-up-to-do) | skip | Competitive landscape commentary, not pm craft |
| 2026-01-15 | AI Can Build Anything. Social Dandelions Decide What Spreads. | Lewis Kallow | [link](https://every.to/p/ai-can-build-anything-social-dandelions-decide-what-spreads) | scrape | [2026-01-15-social-dandelions-decide-what-spreads.md](2026-01-15-social-dandelions-decide-what-spreads.md) |
| 2026-01-14 | Why Your AI Learning Projects Keep Fizzling Out | Rhea Purohit (Nir Zicherman) | [link](https://every.to/podcast/why-your-ai-learning-projects-keep-fizzling-out) | scrape | [2026-01-14-why-ai-learning-projects-fizzle.md](2026-01-14-why-ai-learning-projects-fizzle.md) |
| 2026-01-13 | Go Agent-native With Every | Austin Tedesco | [link](https://every.to/on-every/go-agent-native-with-every) | skip | Every promotion/event |
| 2026-01-13 | Vibe Check: Claude Cowork Is Claude Code for the Rest of Us | Katie Parrott | [link](https://every.to/vibe-check/vibe-check-claude-cowork-is-claude-code-for-the-rest-of-us) | skip | Tool vibe check |
| 2026-01-12 | The Boring Businesses That Will Dominate the AI Era | Tina He | [link](https://every.to/thesis/the-boring-businesses-that-will-dominate-the-ai-era) | scrape | [2026-01-12-boring-businesses-dominate-ai-era.md](2026-01-12-boring-businesses-dominate-ai-era.md) |
| 2026-02-01 | Claude Code in a Trenchcoat | Kieran Klaassen, Rhea Purohit | [link](https://every.to/context-window/claude-code-in-a-trenchcoat) | skip | Newsletter digest — ⚠️ incorrectly captured in Feb 15 run; source file marked `irrelevant` |
| 2026-01-09 | Agent-native Architectures: How to Build Apps After the End of Code | Dan Shipper | [link](https://every.to/chain-of-thought/agent-native-architectures-how-to-build-apps-after-the-end-of-code) | scrape | [2026-01-09-agent-native-architectures.md](2026-01-09-agent-native-architectures.md) |
| 2026-01-08 | The Heyday of the Writing-first Practitioner | Eleanor Warnock | [link](https://every.to/p/the-heyday-of-the-writing-first-practitioner) | scrape | [2026-01-08-heyday-writing-first-practitioner.md](2026-01-08-heyday-writing-first-practitioner.md) |
| 2026-01-08 | For Paid Subscribers Only: Every's Cursor Camp | Every Staff | [link](https://every.to/on-every/for-paid-subscribers-only-every-s-cursor-camp) | skip | Every event promo |
| 2026-01-07 | Reid Hoffman Makes Five Predictions About AI In 2026 | Rhea Purohit (Reid Hoffman) | [link](https://every.to/podcast/reid-hoffman-makes-five-predictions-about-ai-in-2026) | scrape | [2026-01-07-reid-hoffman-five-predictions-ai-2026.md](2026-01-07-reid-hoffman-five-predictions-ai-2026.md) |
| 2026-01-06 | I Asked Claude the Question I Could Never Ask My Boss | Katie Parrott | [link](https://every.to/working-overtime/i-asked-claude-the-question-i-could-never-ask-my-boss) | scrape | [2026-01-06-i-asked-claude-question-i-could-never-ask-boss.md](2026-01-06-i-asked-claude-question-i-could-never-ask-boss.md) |
| 2026-01-05 | How AI Made Pricing Hard Again | Anh-Tho Chuong | [link](https://every.to/p/how-ai-made-pricing-hard-again) | scrape | [2026-01-05-how-ai-made-pricing-hard-again.md](2026-01-05-how-ai-made-pricing-hard-again.md) — partial paywall |
| 2025-12-23 | Four Predictions for How AI Will Change Software in 2026 | Rhea Purohit | [link](https://every.to/podcast/four-predictions-for-how-ai-will-change-software-in-2026) | scrape | [2025-12-23-four-predictions-ai-change-software-2026.md](2025-12-23-four-predictions-ai-change-software-2026.md) |
| 2025-12-23 | Every's 2026 Predictions | Every Staff | [link](https://every.to/context-window/every-s-2026-predictions) | skip | Every's internal team predictions |
| 2025-12-22 | Reid Hoffman on How AI Might Answer Our Biggest Questions | Dan Shipper (Reid Hoffman) | [link](https://every.to/podcast/reid-hoffman-on-how-ai-might-answer-our-biggest-questions-520668b0-3ef7-41d6-b402-2c2ddd832ead) | skip | Philosophy, not pm craft |
| 2025-12-22 | Every 2025: Our Year by the Numbers | Every Staff | [link](https://every.to/on-every/2025-year-in-review) | skip | Every year-in-review |
| 2025-12-19 | GPT Image 1.5 Shines (If You Do This) | Every Staff | [link](https://every.to/context-window/gpt-image-1-5-shines-if-you-do-this) | skip | Newsletter digest |
| 2025-12-19 | OpenAI Gave Us a Glimpse Into Their AI Coding Playbook | Katie Parrott | [link](https://every.to/source-code/openai-gave-us-a-glimpse-into-their-ai-coding-playbook) | scrape | [2025-12-19-openai-gave-glimpse-ai-coding-playbook.md](2025-12-19-openai-gave-glimpse-ai-coding-playbook.md) |

### Page 3 — Dec 18 to Nov 20, 2025

| Date | Title | Author | URL | Decision | Reason / Source File |
|---|---|---|---|---|---|
| 2025-12-18 | How AI Can Cut Your Planning Cycle From Two Weeks to Two Days | Austin Tedesco | [link](https://every.to/p/how-ai-can-cut-your-planning-cycle-from-two-weeks-to-two-days) | scrape | [2025-12-18-how-ai-can-cut-planning-cycle-two-weeks-to-two-days.md](2025-12-18-how-ai-can-cut-planning-cycle-two-weeks-to-two-days.md) |
| 2025-12-18 | For All Subscribers: Every's Q4 Demo Day | Every Staff | [link](https://every.to/on-every/for-all-subscribers-every-s-q4-demo-day) | skip | Every event promo |
| 2025-12-17 | What Jhana Meditation Feels Like—From the Inside Out | Rhea Purohit (Stephen Zerfas) | [link](https://every.to/podcast/he-got-into-a-jhana-live-on-the-show-and-explains-how-you-can-too) | skip | Meditation topic, not ai-pm |
| 2025-12-16 | I Talked to More Than 100 Companies About AI—Here's What's Actually Working | Natalia Quintero | [link](https://every.to/p/i-talked-to-more-than-100-companies-about-ai-here-s-what-s-actually-working) | scrape | [2025-12-16-i-talked-to-100-companies-about-ai-whats-working.md](2025-12-16-i-talked-to-100-companies-about-ai-whats-working.md) |
| 2025-12-15 | What Becomes Valuable When AI Makes Creative Work Easy | Jack Cheng | [link](https://every.to/p/what-becomes-valuable-when-ai-makes-creative-work-easy) | skip | Creativity essay, not pm craft |
| 2025-12-13 | Who Even Codes Anymore? | Every Staff | [link](https://every.to/context-window/who-even-codes-anymore) | skip | Newsletter digest |
| 2025-12-12 | How This Venture Capitalist Sees Into the Post-software Future | Rhea Purohit (Sumeet Singh) | [link](https://every.to/thesis/how-this-venture-capitalist-sees-into-the-post-software-future) | scrape | [2025-12-12-vc-sees-into-post-software-future-sumeet-singh.md](2025-12-12-vc-sees-into-post-software-future-sumeet-singh.md) |
| 2025-12-11 | Vibe Check: GPT-5.2 Is an Incremental Upgrade | Katie Parrott | [link](https://every.to/vibe-check/vibe-check-gpt-5-2-is-an-incremental-upgrade) | skip | Model vibe check |
| 2025-12-11 | Compound Engineering: How Every Codes With Agents | Dan Shipper | [link](https://every.to/chain-of-thought/compound-engineering-how-every-codes-with-agents) | skip | ⚠️ Duplicate of Jan 30 article (same content, different URL); scraping the Jan 30 version |
| 2025-12-10 | She Turned Her Whole Life Into Training Data—For an AI Baby | Rhea Purohit (Sarah Rose Siskind) | [link](https://every.to/podcast/she-turned-her-whole-life-into-training-data-for-an-ai-baby) | skip | Personal story, not pm craft |
| 2025-12-09 | How Every Is Harnessing the World-changing Shift of Opus 4.5 | Katie Parrott | [link](https://every.to/source-code/how-every-is-harnessing-the-world-changing-shift-of-opus-4-5) | skip | Every's internal workflow, company-specific |
| 2025-12-08 | Two Ways to Win in the Post-software Era | Sumeet Singh | [link](https://every.to/thesis/two-ways-to-win-in-the-post-software-era) | scrape | [2025-12-08-two-ways-to-win-post-software-era.md](2025-12-08-two-ways-to-win-post-software-era.md) |
| 2025-12-05 | The Week the World Changed | Every Staff | [link](https://every.to/context-window/the-week-the-world-changed) | skip | Newsletter digest |
| 2025-12-05 | This Prompt Optimizer Learns From Its Mistakes Like DNA | Mike Taylor | [link](https://every.to/also-true-for-humans/this-prompt-optimizer-learns-from-its-mistakes-like-dna) | scrape | [2025-12-05-gepa-prompt-optimizer-learns-from-mistakes-like-dna.md](2025-12-05-gepa-prompt-optimizer-learns-from-mistakes-like-dna.md) |
| 2025-12-04 | Opus 4.5 Collapsed Six Months of Development Work Into One Week | Dan Shipper | [link](https://every.to/chain-of-thought/opus-4-5-collapsed-six-months-of-development-work-into-one-week) | scrape | [2025-12-04-opus-45-collapsed-six-months-development-one-week.md](2025-12-04-opus-45-collapsed-six-months-development-one-week.md) |
| 2025-12-03 | Anthropic's Newest Model Blew This Founder's Mind—And Made Him Uncomfortable | Rhea Purohit (Paul Ford) | [link](https://every.to/podcast/anthropic-s-newest-model-blew-this-founder-s-mind-and-made-him-uncomfortable-273eac07-071c-4638-b6fe-a7a72541dd5d) | skip | Reaction piece, not pm craft |
| 2025-12-02 | Think First, AI Second | Ines Lee | [link](https://every.to/p/think-first-ai-second) | scrape | [2025-12-02-think-first-ai-second.md](2025-12-02-think-first-ai-second.md) |
| 2025-12-01 | Claude Code: The Most Common Questions Beginners Ask | Nityesh Agarwal | [link](https://every.to/source-code/claude-code-the-most-common-questions-beginners-ask) | scrape | [2025-12-01-claude-code-common-questions-beginners.md](2025-12-01-claude-code-common-questions-beginners.md) |
| 2025-11-30 | A Feast of Takes on Opus 4.5 | Every Staff | [link](https://every.to/context-window/a-feast-of-takes-on-opus-4-5) | skip | Newsletter digest |
| 2025-11-25 | Inside The Browser Company: Why They Killed Arc to Build Dia | Rhea Purohit (Josh Miller, Hursh Agrawal) | [link](https://every.to/podcast/inside-the-browser-company-why-they-killed-arc-to-build-dia-cde1410f-74b8-4f01-99f9-54f1130119c0) | scrape | [2025-11-25-inside-browser-company-killed-arc-build-dia.md](2025-11-25-inside-browser-company-killed-arc-build-dia.md) |
| 2025-11-25 | The AI Browsers That Made It Into Our Daily Workflow | Rhea Purohit | [link](https://every.to/vibe-check/the-ai-browsers-that-made-it-into-our-daily-workflow) | skip | Tool roundup vibe check |
| 2025-11-24 | Vibe Check: Opus 4.5 Is the Coding Model We've Been Waiting For | Katie Parrott | [link](https://every.to/vibe-check/vibe-check-opus-4-5-is-the-coding-model-we-ve-been-waiting-for) | skip | Model vibe check |
| 2025-11-23 | ChatGPT Has Entered the Chat | Every Staff | [link](https://every.to/context-window/chatgpt-has-entered-the-chat) | skip | Newsletter digest |
| 2025-11-20 | Frankenstein Is Not Your AI Metaphor (At Least, Not Like That) | Katie Parrott | [link](https://every.to/working-overtime/frankenstein-is-not-your-ai-metaphor-at-least-not-like-that) | skip | Cultural essay, not pm craft |

### Page 4 — Nov 19 to Oct 26, 2025

| Date | Title | Author | URL | Decision | Reason / Source File |
|---|---|---|---|---|---|
| 2025-11-19 | Vibe Check: Gemini 3 Pro, A Reliable Workhorse With Surprising Flair | Rhea Purohit | [link](https://every.to/vibe-check/vibe-check-gemini-3-pro-a-reliable-workhorse-with-surprising-flair) | skip | Model vibe check |
| 2025-11-19 | How Two Engineers Ship Like a Team of 15 With AI Agents | Rhea Purohit (Kieran Klaassen, Nityesh Agarwal) | [link](https://every.to/podcast/how-two-engineers-ship-like-a-team-of-15-with-ai-agents-7bc186bd-b5ea-40cd-9690-963845203f80) | scrape | [2025-11-19-how-two-engineers-ship-like-team-of-15-ai-agents.md](2025-11-19-how-two-engineers-ship-like-team-of-15-ai-agents.md) |
| 2025-11-18 | When AI Can Do Your Job, Who Else Are You? | Danny Aziz | [link](https://every.to/source-code/when-ai-can-do-your-job-who-else-are-you) | scrape | [2025-11-18-when-ai-can-do-your-job-who-else-are-you.md](2025-11-18-when-ai-can-do-your-job-who-else-are-you.md) |
| 2025-11-16 | Austin Tedesco Joins Every as Head of Growth | Dan Shipper | [link](https://every.to/on-every/austin-tedesco-joins-every-as-head-of-growth) | skip | Every company announcement |
| 2025-11-16 | Checking In on GPT-5.1 | Every Staff | [link](https://every.to/context-window/checking-in-on-gpt-5-1) | skip | Newsletter digest |
| 2025-11-14 | AI Ran Out of Internet. Now It's Learning by Playing Games Again. | Alex Duffy | [link](https://every.to/playtesting/ai-ran-out-of-internet-now-it-s-learning-by-playing-games-again) | scrape | [2025-11-14-ai-ran-out-of-internet-learning-by-playing-games.md](2025-11-14-ai-ran-out-of-internet-learning-by-playing-games.md) |
| 2025-11-13 | AI Solved the Problem I Couldn't Explain to Managers | Katie Parrott | [link](https://every.to/working-overtime/ai-isn-t-making-me-more-productive-it-s-making-it-possible-to-work-at-all) | scrape | [2025-11-13-ai-solved-problem-i-couldnt-explain-to-managers.md](2025-11-13-ai-solved-problem-i-couldnt-explain-to-managers.md) |
| 2025-11-12 | He Built AI Agents to Launch a Million Businesses | Rhea Purohit (Henrik Werdelin) | [link](https://every.to/podcast/he-built-ai-agents-to-launch-a-million-businesses) | scrape | [2025-11-12-he-built-ai-agents-launch-million-businesses-werdelin.md](2025-11-12-he-built-ai-agents-launch-million-businesses-werdelin.md) |
| 2025-11-10 | Where Explanations End | Dan Shipper | [link](https://every.to/chain-of-thought/where-explanations-end) | skip | Philosophical essay |
| 2025-11-09 | A Good Start for Claude Skills | Every Staff | [link](https://every.to/context-window/a-good-start-for-claude-skills) | skip | Newsletter digest |
| 2025-11-07 | Teach Your AI to Think Like a Senior Engineer | Kieran Klaassen | [link](https://every.to/source-code/teach-your-ai-to-think-like-a-senior-engineer) | skip | ⚠️ Duplicate of Jan 29 article — scraping the later version |
| 2025-11-06 | Stop Coding and Start Planning | Kieran Klaassen | [link](https://every.to/source-code/stop-coding-and-start-planning) | skip | ⚠️ Duplicate of Jan 28 article — scraping the later version |
| 2025-11-05 | What Jason Fried Learned From 26 Years of Building Great Products | Rhea Purohit (Jason Fried) | [link](https://every.to/podcast/what-jason-fried-learned-from-26-years-of-building-great-products) | scrape | [2025-11-05-what-jason-fried-learned-26-years-building-products.md](2025-11-05-what-jason-fried-learned-26-years-building-products.md) |
| 2025-11-04 | The Tool That Lets You Switch Models Without Losing Your Place | Katie Parrott | [link](https://every.to/source-code/the-tool-that-lets-you-switch-models-without-losing-your-place) | scrape | [2025-11-04-droid-tool-switch-models-without-losing-your-place.md](2025-11-04-droid-tool-switch-models-without-losing-your-place.md) |
| 2025-11-03 | Vibe Check: Claude Skills Need a 'Share' Button | Katie Parrott | [link](https://every.to/vibe-check/vibe-check-claude-skills-need-a-share-button) | skip | Tool vibe check |
| 2025-11-02 | The Droid You're Looking For | Every Staff | [link](https://every.to/context-window/the-droid-you-re-looking-for) | skip | Newsletter digest |
| 2025-10-31 | How Tools Shape How We See the World | Dan Shipper | [link](https://every.to/chain-of-thought/how-tools-shape-how-we-see-the-world) | scrape | [2025-10-31-how-tools-shape-how-we-see-the-world.md](2025-10-31-how-tools-shape-how-we-see-the-world.md) |
| 2025-10-30 | Vibe Check: I Canceled Two AI Max Plans for Factory's Coding Agent Droid | Danny Aziz | [link](https://every.to/vibe-check/vibe-check-i-canceled-two-ai-max-plans-for-factory-s-coding-agent-droid) | skip | Tool vibe check |
| 2025-10-30 | For Paid Subscribers Only: Every's Droid Camp | Every Staff | [link](https://every.to/on-every/for-paid-subscribers-only-every-s-droid-camp) | skip | Every event promo |
| 2025-10-29 | Vibe Check: Cursor 2.0 and Composer 1 Alpha | Rhea Purohit | [link](https://every.to/vibe-check/vibe-check-cursor-2-0-and-composer-1-alpha) | skip | Tool vibe check |
| 2025-10-29 | How to Use Claude Code Like the People Who Built It | Rhea Purohit (Cat Wu, Boris Cherny) | [link](https://every.to/podcast/how-to-use-claude-code-like-the-people-who-built-it) | scrape | [2025-10-29-how-to-use-claude-code-like-people-who-built-it.md](2025-10-29-how-to-use-claude-code-like-people-who-built-it.md) |
| 2025-10-28 | How My Company Turned a Data Crisis Into an AI-native Rebirth | Stella Garber | [link](https://every.to/p/how-my-company-turned-a-data-crisis-into-an-ai-native-rebirth) | scrape | [2025-10-28-how-company-turned-data-crisis-ai-native-rebirth.md](2025-10-28-how-company-turned-data-crisis-ai-native-rebirth.md) |
| 2025-10-27 | Inside the AI Workflows of Every's Six Engineers | Rhea Purohit | [link](https://every.to/source-code/inside-the-ai-workflows-of-every-s-six-engineers) | skip | Every's internal workflows specifically |
| 2025-10-26 | OpenAI's Atlas: Shrug or No Shrug? | Every Staff | [link](https://every.to/context-window/openai-s-atlas-shrug-or-no-shrug) | skip | Newsletter digest |

### Page 5 — Oct 24 to Oct 1, 2025

| Date | Title | Author | URL | Decision | Reason / Source File |
|---|---|---|---|---|---|
| 2025-10-24 | Seeing Creativity Like a Language Model | Dan Shipper | [link](https://every.to/chain-of-thought/seeing-creativity-like-a-language-model) | scrape | [2025-10-24-seeing-creativity-like-a-language-model.md](2025-10-24-seeing-creativity-like-a-language-model.md) |
| 2025-10-23 | We Tested Claude Sonnet 4.5 for Writing and Editing | Katie Parrott | [link](https://every.to/vibe-check/vibe-check-we-tested-claude-sonnet-4-5-for-writing-and-editing) | skip | Model vibe check |
| 2025-10-22 | He Built an AI Ghostwriter With Taste | Rhea Purohit (Danny Aziz) | [link](https://every.to/podcast/spiral-s-creator-on-why-better-writing-means-better-thinking) | scrape | [2025-10-22-he-built-ai-ghostwriter-with-taste-danny-aziz.md](2025-10-22-he-built-ai-ghostwriter-with-taste-danny-aziz.md) |
| 2025-10-21 | Vibe Check: OpenAI's New AI Browser, Atlas | Dan Shipper | [link](https://every.to/vibe-check/vibe-check-openai-s-new-ai-browser-atlas) | skip | Tool vibe check |
| 2025-10-21 | Introducing Spiral v3: An AI Writing Partner With Taste | Dan Shipper | [link](https://every.to/on-every/introducing-spiral-v3-an-ai-writing-partner-with-taste) | skip | Every product launch (Spiral) |
| 2025-10-20 | Vibe Check: Claude Code Now Works on Mobile and the Web | Dan Shipper | [link](https://every.to/vibe-check/vibe-check-we-spent-a-weekend-trying-to-code-from-our-phones) | skip | Tool vibe check |
| 2025-10-17 | Playing Games With AI | Every Staff | [link](https://every.to/context-window/playing-games-with-ai) | skip | Newsletter digest |
| 2025-10-17 | Seeing Business Like a Language Model | Dan Shipper | [link](https://every.to/chain-of-thought/seeing-business-like-a-language-model) | scrape | [2025-10-17-seeing-business-like-a-language-model.md](2025-10-17-seeing-business-like-a-language-model.md) |
| 2025-10-16 | OpenAI Made Video Creation Effortless—Here's What Happened Next | Rhea Purohit | [link](https://every.to/vibe-check/openai-made-video-creation-effortless-here-s-what-happened-next) | skip | Not pm craft |
| 2025-10-15 | Our New Incubation Raised $3.6 Million to Teach AIs to Play Games | Dan Shipper | [link](https://every.to/on-every/our-new-incubation-raised-3-6-million-to-teach-ais-to-play-games) | skip | Every company announcement |
| 2025-10-15 | How Playing Games Is Making AI Smarter | Rhea Purohit (Alex Duffy) | [link](https://every.to/podcast/we-taught-ai-to-play-games-now-it-s-a-3-6-million-company-97fa0f2d-0c83-42e7-bcda-8c877eebbd27) | skip | Game-based AI training at Good Start Labs (Every subsidiary) |
| 2025-10-15 | Vibe Check: Anthropic Cooked on Claude Haiku 4.5 | Dan Shipper | [link](https://every.to/vibe-check/vibe-check-claude-haiku-4-5-anthropic-cooked) | skip | Model vibe check |
| 2025-10-14 | A Founder's Guide to Finding a Great Name | Willem Van Lancker | [link](https://every.to/thesis/a-founder-s-guide-to-finding-a-great-name) | skip | Naming, not pm craft |
| 2025-10-11 | Robots Are Coming! (No, They're Not!) | Every Staff | [link](https://every.to/context-window/robots-are-coming-no-they-re-not) | skip | Newsletter digest |
| 2025-10-10 | Seeing Science Like a Language Model | Dan Shipper | [link](https://every.to/chain-of-thought/seeing-science-like-a-language-model) | scrape | [2025-10-10-seeing-science-like-a-language-model.md](2025-10-10-seeing-science-like-a-language-model.md) |
| 2025-10-09 | How to Use Claude Code for Everyday Tasks—No Programming Required | Katie Parrott | [link](https://every.to/source-code/how-to-use-claude-code-for-everyday-tasks-no-programming-required) | scrape | [2025-10-09-how-to-use-claude-code-everyday-tasks-no-programming.md](2025-10-09-how-to-use-claude-code-everyday-tasks-no-programming.md) |
| 2025-10-08 | How Box Is Building an AI-first Company—Without Cutting Jobs | Rhea Purohit (Aaron Levie) | [link](https://every.to/podcast/box-ceo-aaron-levie-on-why-ai-agents-won-t-take-your-job) | scrape | [2025-10-08-box-building-ai-first-company-without-cutting-jobs-aaron-levie.md](2025-10-08-box-building-ai-first-company-without-cutting-jobs-aaron-levie.md) |
| 2025-10-07 | Smuggled Intelligence | Dan Shipper | [link](https://every.to/chain-of-thought/smuggled-intelligence) | skip | AI jobs opinion, not pm craft |
| 2025-10-06 | Vibe Check: OpenAI DevDay 2025 | Dan Shipper | [link](https://every.to/vibe-check/vibe-check-openai-devday-2025) | skip | Event vibe check |
| 2025-10-05 | You Down With MCP? | Every Staff | [link](https://every.to/context-window/you-down-with-mcp) | skip | Newsletter digest |
| 2025-10-03 | Seeing Like a Language Model | Dan Shipper | [link](https://every.to/chain-of-thought/seeing-like-a-language-model) | scrape | [2025-10-03-seeing-like-a-language-model.md](2025-10-03-seeing-like-a-language-model.md) |
| 2025-10-03 | For Paid Subscribers Only: Every's Claude Code Camp III | Every Staff | [link](https://every.to/on-every/for-paid-subscribers-only-every-s-claude-code-camp-iii) | skip | Every event promo |
| 2025-10-02 | I Inherited a Broken App—And Made It Mine | Yash Poojary | [link](https://every.to/source-code/i-inherited-a-broken-app-and-made-it-mine) | skip | Personal app story, not pm craft |
| 2025-10-01 | He's Building the Plumbing For AI to Use the Internet | Rhea Purohit (Alex Rattray) | [link](https://every.to/podcast/he-s-building-the-plumbing-for-ai-to-use-the-internet) | scrape | [2025-10-01-building-plumbing-for-ai-to-use-internet-alex-rattray.md](2025-10-01-building-plumbing-for-ai-to-use-internet-alex-rattray.md) |

### Page 6 — Sep 30 to Sep 2, 2025

| Date | Title | Author | URL | Decision | Reason / Source File |
|---|---|---|---|---|---|
| 2025-09-30 | How to Make AI Write Less Like AI | Chris Silvestri | [link](https://every.to/p/how-to-make-ai-write-less-like-ai) | scrape | [2025-09-30-how-to-make-ai-write-less-like-ai.md](2025-09-30-how-to-make-ai-write-less-like-ai.md) |
| 2025-09-29 | Vibe Check: Claude Sonnet 4.5 | Dan Shipper | [link](https://every.to/vibe-check/vibe-check-claude-sonnet-4-5) | skip | Model vibe check |
| 2025-09-28 | Living in a Post-code World | Every Staff | [link](https://every.to/context-window/living-in-a-post-code-world) | skip | Newsletter digest |
| 2025-09-26 | Every's Master Plan: Part II | Dan Shipper | [link](https://every.to/on-every/every-s-master-plan-part-ii) | skip | Every company strategy |
| 2025-09-25 | I've Stopped Writing Prompts—DSPy Does It Better | Mike Taylor | [link](https://every.to/also-true-for-humans/i-ve-stopped-writing-prompts-dspy-does-it-better) | scrape | [2025-09-25-ive-stopped-writing-prompts-dspy-does-it-better.md](2025-09-25-ive-stopped-writing-prompts-dspy-does-it-better.md) |
| 2025-09-24 | Cognition's CEO on What Comes After Code | Rhea Purohit (Scott Wu) | [link](https://every.to/podcast/how-cognition-built-the-world-s-first-coding-agent-before-claude-code) | scrape | [2025-09-24-cognitions-ceo-on-what-comes-after-code-scott-wu.md](2025-09-24-cognitions-ceo-on-what-comes-after-code-scott-wu.md) |
| 2025-09-23 | You're Probably Using AI Wrong | Rhea Purohit | [link](https://every.to/learning-curve/you-re-probably-using-ai-wrong-dff84293-9edc-4da5-8732-71bd8d5d5b96) | scrape | [2025-09-23-youre-probably-using-ai-wrong.md](2025-09-23-youre-probably-using-ai-wrong.md) |
| 2025-09-22 | I Fed My Essays to ChatGPT Until It Learned My Voice | Katie Parrott | [link](https://every.to/working-overtime/i-fed-my-essays-to-chatgpt-until-it-learned-my-voice) | scrape | [2025-09-22-i-fed-my-essays-to-chatgpt-until-it-learned-my-voice.md](2025-09-22-i-fed-my-essays-to-chatgpt-until-it-learned-my-voice.md) |
| 2025-09-21 | OpenAI's Codex Is Now a Claude Code Competitor | Every Staff | [link](https://every.to/context-window/openai-s-codex-is-now-a-claude-code-competitor) | skip | Newsletter digest |
| 2025-09-18 | Launch Day Lies—Day Two Tells the Truth | Naveen Naidu | [link](https://every.to/source-code/launch-day-lies-day-two-tells-the-truth) | scrape | [2025-09-18-launch-day-lies-day-two-tells-the-truth.md](2025-09-18-launch-day-lies-day-two-tells-the-truth.md) |
| 2025-09-17 | He Got Thousands of Users Before His AI App Even Launched | Rhea Purohit (Naveen Naidu) | [link](https://every.to/podcast/he-got-thousands-of-users-before-his-app-even-launched) | scrape | [2025-09-17-he-got-thousands-of-users-before-app-launched-naveen-naidu.md](2025-09-17-he-got-thousands-of-users-before-app-launched-naveen-naidu.md) |
| 2025-09-16 | Introducing Monologue: Effortless Voice Dictation | Dan Shipper | [link](https://every.to/on-every/introducing-monologue-effortless-voice-dictation) | skip | Every product launch (Monologue) |
| 2025-09-15 | Vibe Check: GPT-5 Codex Can Code for 35 Minutes Straight—If You Ask Nicely | Dan Shipper | [link](https://every.to/vibe-check/gpt-5-codex-knows-when-to-think-hard-and-when-not-to) | skip | Model vibe check |
| 2025-09-14 | A Clean, Well-lighted Place on the Internet | Every Staff | [link](https://every.to/context-window/a-clean-well-lighted-place-on-the-internet) | skip | Newsletter digest |
| 2025-09-11 | Build Places, Not Products | Lucas Crespo | [link](https://every.to/source-code/build-places-not-products) | scrape | [2025-09-11-build-places-not-products.md](2025-09-11-build-places-not-products.md) |
| 2025-09-10 | How to Use Claude Code as a Second Brain | Rhea Purohit (Noah Brier) | [link](https://every.to/podcast/how-to-use-claude-code-as-a-thinking-partner) | scrape | [2025-09-10-how-to-use-claude-code-as-second-brain-noah-brier.md](2025-09-10-how-to-use-claude-code-as-second-brain-noah-brier.md) |
| 2025-09-09 | Why 95 Percent of AI Pilots Fail—And How to Avoid It | Marc Malott | [link](https://every.to/p/why-95-percent-of-ai-pilots-fail-and-how-to-avoid-it-happening-to-you) | scrape | [2025-09-09-why-95-percent-ai-pilots-fail.md](2025-09-09-why-95-percent-ai-pilots-fail.md) |
| 2025-09-08 | How I Run Three AI Models in Parallel Without Losing My Mind | Katie Parrott | [link](https://every.to/working-overtime/how-i-run-three-ai-models-in-parallel-without-losing-my-mind) | scrape | [2025-09-08-how-i-run-three-ai-models-in-parallel.md](2025-09-08-how-i-run-three-ai-models-in-parallel.md) |
| 2025-09-07 | Why I Started Talking to My Computer | Every Staff | [link](https://every.to/context-window/why-i-started-talking-to-my-computer) | skip | Newsletter digest |
| 2025-09-05 | Silicon Valley's Top Coaches Want You to Stop Fearing AI | Rhea Purohit (Joe Hudson, Jonny Miller, Steve Schlafman) | [link](https://every.to/podcast/silicon-valley-s-top-coaches-want-you-to-stop-fearing-ai) | scrape | [2025-09-05-silicon-valley-coaches-stop-fearing-ai.md](2025-09-05-silicon-valley-coaches-stop-fearing-ai.md) |
| 2025-09-04 | How AI Image Models Work | Nir Zicherman | [link](https://every.to/p/how-ai-image-models-work-49b41bc0-2365-4157-a6d7-3f8adaac787f) | skip | Technical explainer, not pm craft |
| 2025-09-04 | For Paid Subscribers Only: Every Demo Day | Every Staff | [link](https://every.to/on-every/for-paid-subscribers-only-every-demo-day) | skip | Every event promo |
| 2025-09-03 | This AI Makes a Video Game World in 40 Milliseconds | Rhea Purohit (Dean Leitersdorf) | [link](https://every.to/podcast/this-ai-makes-a-video-game-world-in-40-milliseconds) | skip | Gaming tech, not pm craft |
| 2025-09-02 | I Started Talking to My Computer Instead of Typing. It Changed How I Think. | Katie Parrott | [link](https://every.to/working-overtime/i-didn-t-know-typing-held-me-back-until-i-started-thinking-out-loud) | scrape | [2025-09-02-i-started-talking-to-computer-instead-of-typing.md](2025-09-02-i-started-talking-to-computer-instead-of-typing.md) |

---

## Summary

**Scrape run 2026-02-17**

| | Count |
|---|---|
| Total articles considered | 144 |
| Scraped | 57 |
| Skipped | 87 |

**Skip reasons breakdown:**
- Newsletter digests (context-window / Every Staff) | 23
- Model/tool vibe checks | 22
- Every product/event/company announcements (on-every) | 16
- Philosophy essays or off-topic content | 14
- Duplicates (same article, different URL slug) | 3
- Every-internal content (specific to Every's workflows) | 3
- Other (naming, gaming tech, personal stories) | 6

**Next run guidance:**
- Start from 2026-02-17 — check for new articles above that date
- Add new rows at the top of the relevant page section
- Update "scrape_range" and "scrape_pages" in frontmatter
- Column prefix rules in the Column Guide above are reliable heuristics
