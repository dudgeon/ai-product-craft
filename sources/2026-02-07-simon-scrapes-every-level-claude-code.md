---
title: "Every Level of Claude Code Explained in 39 Minutes"
created: 2026-02-16
updated: 2026-02-16
template: templates/source.md
template_version: 3
tags: [source, ai-pm, claude-code, agent-workflows, automation]
status: unread
source_type: video
source_url: "https://www.youtube.com/watch?v=Y09u_S3w2c8"
archive_url: "domains/professional-development/ai-pm/sources/2026-02-07-simon-scrapes-every-level-claude-code.md"
author: "Simon Scrapes"
published: 2026-02-07
discovered: 2026-02-16
companion_url: "https://scrapeshq.notion.site/Every-Level-of-Claude-Code-Explained-in-39-Minutes-3007821711818048b119f78d5cc725ff"
summary: "Seven-level progression framework for Claude Code mastery: (1) intentional prompting, (2) CLAUDE.md personalization, (3) slash commands/skills/hooks for repeatability, (4) MCP server integrations, (5) planning mode and project frameworks like GSD, (6) multi-agent teams with sub-agents, (7) fully autonomous pipelines via Ralph loop. Uses social media content creation as the running example throughout. Core thesis: most users plateau at level 2-3; the real leverage comes from skills, hooks, agent teams, and autonomous loops."
domain: professional-development
project: ai-pm
---

# Every Level of Claude Code Explained in 39 Minutes

**By**: Simon Scrapes (Simon Scrapes | AI Automation)
**Source**: [YouTube](https://www.youtube.com/watch?v=Y09u_S3w2c8) | [Notion companion page](https://scrapeshq.notion.site/Every-Level-of-Claude-Code-Explained-in-39-Minutes-3007821711818048b119f78d5cc725ff)
**Type**: video (with structured companion resource)

## Summary

*Fill after reading/watching.*

## Key Ideas Extracted

*Fill during processing. Each idea links to a knowledge entry.*

## Notes

*Your annotations, reactions, questions, disagreements.*

## Raw Content

*Hybrid source: structured content from the Notion companion page, enriched with key details and quotes from the video transcript. The Notion page provides clean code examples and structured guidance; the transcript adds conversational context and verbal explanations.*

**Video**: 39:22, 68K+ views in first 8 days. Channel has 39.5K subscribers.

**Chapter Timestamps**:
- 00:00 - Introduction
- 00:41 - Level 1: The One Thing You Need To Know
- 03:25 - Level 2: Personalizing CLAUDE for better responses
- 10:25 - Level 3: Slash Commands, Skills & Hooks - Repeatability
- 21:21 - Level 4: Connecting Claude Code to Your Apps (MCPs)
- 26:18 - Level 5: Move from Executor to Supervisor
- 29:34 - Level 6: Agent Teams
- 35:57 - Level 7: Fully Autonomous Systems

---

### Introduction

From the transcript: "I've spent over 150 hours now in Claude Code, not just building with it, but studying every single major resource on it. I've broken down the creator Boris Cherny's post, tested real workflows from top builders, and watched every single master Claude tutorial that I could find. And here's what most people miss. Even if you think you're using Claude Code well today, you're probably stuck at level two or level three. This video shows you what's beyond that."

---

### Level 1: The One Thing You Need To Know (0:41)

**Core concept**: Prompting with intent, not just asking questions.

**Quick Installation**:
- Native installer (no Node.js required): `curl -fsSL https://claude.ai/install.sh | bash`
- With npm (requires Node.js 18+): `npm install -g @anthropic-ai/claude-code`

Level 1 is about intentional prompting. From the transcript, the key distinction is prompting with intent vs. just chatting. You provide Claude Code with clear context about your project, your goals, and what you specifically need done. The emphasis is on treating it as a capable agent rather than a chatbot.

---

### Level 2: Personalizing CLAUDE for Better Responses (3:25)

**Core concept**: The CLAUDE.md file is the first thing Claude reads every session. Get it right and Claude works in your style from the jump.

**The golden rule**: Short. Specific. Only what Claude can't figure out itself.

**Five key questions your CLAUDE.md should answer**:

1. **What is this?** — One line. Orient Claude immediately. Not a paragraph. Not your brand manifesto.

   Example:
   ```
   This project generates daily social media content across LinkedIn, X, and Instagram
   in my brand voice, pulling topics from a content calendar in Notion.
   ```

2. **How do I run things?** — The exact steps. Nothing Claude has to guess.

   Example:
   ```
   - Content calendar lives in Notion — pull topics from the "Ready to Write" view
   - Generated posts go into /output/drafts as markdown files, one per platform
   - Images and brand assets are stored in /assets/brand
   - To preview: open the draft files and review before copying to scheduling tool
   ```

3. **What patterns do I follow?** — This is where the magic happens. Voice, rules, non-negotiables.

   Example — Brand voice:
   ```
   IMPORTANT — follow these exactly:
   - Write like you're talking to one person over coffee, not presenting to a boardroom
   - Use "you" and "I", never "we" or "our team"
   - Short sentences. One idea per sentence. Punch, don't waffle.
   - OK to start sentences with "And", "But", "So"
   - Never use: "unlock", "leverage", "game-changer", "synergy", "deep dive"
   - Swearing is fine occasionally on X. Never on LinkedIn or Instagram.
   ```

   Example — Platform formatting:
   ```
   - LinkedIn: hook line first, then line break, then body. End with a question or CTA.
   - X: no hashtags, no threads longer than 5 posts, always conversational
   - Instagram: captions under 100 words, 3-5 relevant hashtags at the end only
   - Never use emojis as bullet points. One emoji per post max, if any.
   ```

   Example — Content rules:
   ```
   - Every post must teach something or share a real experience — no fluff
   - Reference specific tools, numbers, or results wherever possible
   - When mentioning AI tools, position them as assistants not replacements
   - My audience is business owners, NOT developers — keep it jargon-free
   ```

4. **What's weird here?** — The gotchas. Things that will trip Claude up because they're counterintuitive.

   Example:
   ```
   - Notion has "Status" and "Post Status" columns — use "Post Status" (the other is legacy)
   - LinkedIn buries posts that start with a link — never open with a URL
   - Topics marked "Repurpose" must be rewritten from a blog in /content/blog, not from scratch
   - The /templates folder has old formats I no longer use — ignore it completely
   ```

5. **How do we work?** — The process. What happens before, during, and after work gets created.

   Example:
   ```
   - Always generate 3 variations of each post so I can pick my favourite
   - File naming: [date]-[platform]-[topic].md (e.g. 2026-02-04-linkedin-claude-code-tips.md)
   - Never publish or schedule anything — drafts only, I review everything
   - If a topic is unclear, write a 1-line interpretation at the top of the draft
   - When repurposing, change the angle — don't just shorten the original
   ```

**"Point, Don't Dump" trick**: Keep CLAUDE.md lean. Tell Claude WHERE to find detail, not the detail itself:
- "For full brand voice guide with examples, see /docs/brand-voice.md"
- "For past top-performing posts to reference, see /content/best-performers/"

**CLAUDE.md Copy-Paste Template** (from the Notion page):
```markdown
# Project
[One sentence: what this does, which platforms, where topics come from]

# How It Works
- [Where the content calendar lives]
- [Where drafts get saved]
- [Where brand assets are stored]

# Brand Voice
IMPORTANT:
- [How you sound — conversational? authoritative? cheeky?]
- [Words/phrases you NEVER use]
- [Sentence style — short and punchy? storytelling?]

# Platform Rules
- LinkedIn: [format, length, CTA style]
- X: [format, hashtag policy, thread rules]
- Instagram: [caption length, hashtag count, tone]

# Gotchas
- [Counterintuitive thing about your setup]
- [Legacy stuff to avoid]
- [Audience assumption Claude might get wrong]

# Workflow
- [How many variations per post]
- [File naming convention]
- [What Claude should never do without your approval]
```

**CLAUDE.md Quick Checklist**:
- Can I read this in 60 seconds?
- Does every line tell Claude something it can't guess?
- Am I under 30 instructions? (20 is ideal)
- Did I include specific examples, not vague rules?
- Would a freelancer taking over find this useful?

**Pro tips from the video**:
- Run `/init` inside Claude Code on existing projects — it reads your files and drafts a CLAUDE.md. Then cut ruthlessly.
- Fix mistakes in real time: "Add to my CLAUDE.md that we never use hashtags on X posts." Claude updates the file for you.
- Add "IMPORTANT:" to critical rules — Anthropic's team confirms this improves instruction-following.
- Drop your 5-10 best outputs into a reference folder — Claude matches your voice better from real examples than written descriptions.
- Build over weeks, not one sitting. Every time Claude writes something off, add a line. Every time a rule never matters, remove it.
- Separate personal from shared: `CLAUDE.md` (checked into repo) for team rules, `CLAUDE.local.md` (gitignored) for personal preferences.

---

### Level 3: Slash Commands, Skills & Hooks — Repeatability (10:25)

**Core concept**: Three mechanisms for building repeatable workflows.

#### Slash Commands

Commands you manually trigger at specific moments. You know exactly when you want them.

Examples:
- `/project:linkedin-post` — "write me 3 LinkedIn posts about this topic"
- `/project:x-thread` — "turn this idea into an X thread"
- `/project:repurpose-blog` — "take this blog post and create platform-specific versions"
- `/project:weekly-batch` — "generate all posts for this week from the Notion calendar"

You're pressing the button. You're saying "do this now."

#### Skills

Background knowledge Claude loads automatically when it's relevant. You don't trigger these — Claude just knows to use them when it needs to.

Unlike commands, skills can include a whole folder of supporting files — example posts, style guides, reference docs — giving Claude much richer context to work from.

Examples:
- `brand-voice` — tone, banned words, sentence style, plus a folder of 10 example posts. Claude pulls this in whenever it's writing any content.
- `platform-rules` — LinkedIn formatting, X thread rules, Instagram caption limits, plus a reference file showing what a perfect post looks like on each platform.
- `audience-profile` — who your readers are, what they care about, their level of tech knowledge, plus supporting docs.

You never type `/brand-voice`. Claude just knows "I'm writing content, I should check the brand voice skill."

**Key distinction**: Use skills when you want to sometimes provide instructions with a relevant skillset. Use slash commands when there are things you specifically know you'll want to invoke at certain points.

#### Hooks

Automatic triggers / mechanical checks that fire when Claude does something. For stuff a bash script can do without needing Claude's brain.

**Banned Word Checker Hook**: Every time Claude writes a file to the drafts folder, automatically scan for banned words and warn before moving on.

```json
{
  "hooks": {
    "PostToolUse": [
      {
        "matcher": "Write",
        "hooks": [
          {
            "type": "command",
            "command": "if echo \"$CLAUDE_FILE_PATH\" | grep -q 'output/drafts'; then grep -inwE 'unlock|leverage|game-changer|synergy|deep dive|seamless|robust|cutting-edge|empower|revolutionise' \"$CLAUDE_FILE_PATH\" && echo '⚠️ BANNED WORDS DETECTED — rewrite before approving' || echo '✅ No banned words found'; fi"
          }
        ]
      }
    ]
  }
}
```

**Word count check hook** — flag any post over the limit:

```json
{
  "hooks": {
    "PostToolUse": [
      {
        "matcher": "Write",
        "hooks": [
          {
            "type": "command",
            "command": "if echo \"$CLAUDE_FILE_PATH\" | grep -q 'output/drafts'; then WC=$(wc -w < \"$CLAUDE_FILE_PATH\"); if [ $WC -gt 200 ]; then echo \"⚠️ Post is $WC words — over 200 word limit\"; fi; fi"
          }
        ]
      }
    ]
  }
}
```

**Auto-format markdown hook** — clean up files with Prettier after every write:

```json
{
  "hooks": {
    "PostToolUse": [
      {
        "matcher": "Write",
        "hooks": [
          {
            "type": "command",
            "command": "if echo \"$CLAUDE_FILE_PATH\" | grep -q '.md$'; then npx prettier --write \"$CLAUDE_FILE_PATH\" 2>/dev/null; fi"
          }
        ]
      }
    ]
  }
}
```

**Pipeline summary**: You run `/linkedin-post`, Claude writes the posts using the humanizer skill and brand-voice skill automatically, and hooks silently check for banned words and word count in the background. The whole pipeline just works.

**The simple way to remember**:
- **Skills** = how Claude thinks (loaded into its brain while working)
- **Hooks** = what happens automatically after Claude acts (bash scripts, no brain needed)
- **Commands** = what you trigger manually

---

### Level 4: Connecting Claude Code to Your Apps — MCPs (21:21)

**Core concept**: An MCP (Model Context Protocol) server is a bridge between Claude Code and an external app.

Instead of copying data out of Airtable and pasting it into Claude, you connect them — and Claude can read your content calendar, check what's been published, pull upcoming topics, and even create new records.

Example MCP configuration:
```json
{
  "mcpServers": {
    "airtable": {
      "command": "npx",
      "args": ["-y", "airtable-mcp-server"],
      "env": {
        "AIRTABLE_API_KEY": "your_airtable_personal_access_token"
      }
    }
  }
}
```

MCP servers are readily available: https://github.com/wong2/awesome-mcp-servers

---

### Level 5: Move from Executor to Supervisor (26:18)

**Core concept**: Using planning mode and project frameworks to remove yourself from the thinking overhead.

#### Planning Mode

- Leverages the `askUserQuestions` tool
- Referenced Boris Cherny's writing on planning

#### GSD (Get Shit Done) Framework

Install with: `npx get-shit-done-cc`

Leverages the same `askUserQuestions` feature used in planning mode — but the key difference is the level of detail of the breakdown of the plan, which helps solve the biggest problem with long Claude sessions: **context rot**.

Run through each project phase using the plan, execute, and verify commands in sequence:
- `/gsd:plan phase X`
- `/gsd:execute phase Z`
- `/gsd:verify phase Y`

Context is pulled for each phase from overall project documents:
- `ROADMAP.md`
- `REQUIREMENTS.md`
- `STATE.md`

...as well as phase-specific documents.

---

### Level 6: Agent Teams (29:34)

**Core concept**: Running multiple agents to increase leverage through specialization and parallelism.

From a referenced Reddit thread on sub-agents:

> "Sub-agents are specialized personas that you may want to offload specific types work to fresh contexts backed by a full agent instance. So use subagents to keep your context clean when you want an actual full agent instance to perform something without poisoning your main context (code reviewer, skeptic, testing specialist, language/framework specialist, architect, etc.)"

> "The other half is context isolation (the sub agent doesn't bloat the main agent's context). This makes responses faster and cheaper particularly when working on a problem that requires a lot of expertise. Break it down into components and let agents work on it in parallel."

**Two reasons to run a team**:

1. **To improve output quality (specialist vs generalist)** — Sub-agents: one Claude delegating to specialists within the same session. The main Claude calls the researcher sub-agent, gets the brief back, then uses it to write. All happens in one terminal but context is separated.

2. **To get things done faster (parallel non-dependent tasks)** — Parallel terminals: Tab 1 writes LinkedIn posts, Tab 2 writes Instagram posts. They never interact. The value is speed, not collaboration.

**Example Content Research Team**:

**Researcher** (sub-agent 1) — in-depth research with additional tools:
```markdown
# .claude/agents/content-researcher.md
---
name: content-researcher
description: Researches topics for social media content. Finds angles, stats, trending takes, and competitor examples.
allowed-tools: Read, Grep, Glob, WebSearch, WebFetch
---
# Content Researcher
You are a research specialist for a social media content team.
Your job:
- Find interesting angles on a given topic
- Pull relevant stats, examples, and real-world results
- Check what competitors and influencers are saying
- Summarise findings in a short research brief (under 300 words)
Rules:
- NEVER write the actual post — just deliver the research
- NEVER edit any files — you are read-only
- Always include at least one surprising stat or contrarian angle
- Output your brief as a markdown file in /research/briefs/
```

**Writer** — the main instance.

**Reviewer** (sub-agent 2) — read-only, can only suggest edits:
```markdown
# .claude/agents/content-reviewer.md
---
name: content-reviewer
description: Reviews drafted social media posts against brand voice guidelines and platform rules. Read-only — cannot edit posts.
allowed-tools: Read, Grep, Glob
---
# Content Reviewer
You are a brand voice reviewer for social media content.
Your job:
- Read drafted posts in /output/drafts/
- Check them against the brand-voice skill
- Flag banned words, off-brand tone, or formatting issues
- Check word count against platform limits (LinkedIn: 200, X: 280 chars, IG: 100)
Rules:
- NEVER edit the drafts — only flag issues
- NEVER write new content
- Output your review as a markdown file in /output/reviews/
- Use this format for each post:
  - ✅ Pass or ❌ Fail
  - Issues found (list each one)
  - Suggested fix (describe, don't rewrite)
```

**Task 1 — Sub-agents working together** (single terminal, sequential):

```
Pull an idea from my Airtable content calendar. Use the content-researcher
subagent to research angles on that topic. Then use that research to
/linkedin-post on the topic. Then use the content-reviewer subagent to
review the drafts.
```

**Task 2 — Sub-agents working in parallel** (two terminals, concurrent):

```
# terminal 1
Pull an idea from Ideas table from Airtable and /project:linkedin-post for each one

# terminal 2
Pull an idea from Ideas table from Airtable and /project:linkedin-post for each one
```

Also: leverage specialized agents others have built: https://github.com/wshobson/agents

---

### Level 7: Fully Autonomous Systems (35:57)

**Core concept**: Claude literally works on the problem while you sleep.

#### The Ralph Loop

How it works: You write a list of user stories in a simple JSON file — each one has a title, description, and acceptance criteria. Ralph reads this list, picks the first incomplete task, implements it, runs your tests, commits the code, and loops back for the next one. **Each loop starts with a fresh Claude session so there's no context rot.** Progress is tracked in a file that each new session reads, so Claude builds on what the last session learned.

Three files: a bash script, `prd.json` story file, `prompt.md` instructions.

**Install using the plugin**:
```
/plugin marketplace add anthropics/claude-code
/plugin install ralph-wiggum
```

With the plugin installed, you only need to worry about the `prd.json` file:

```json
{
  "project": "Weekly Content Batch - Feb 2026",
  "stories": [
    {
      "id": "post-001",
      "title": "LinkedIn: SaaS vs Automation",
      "description": "Write a LinkedIn post about why businesses waste money on SaaS tools they could replace with simple automations. Use brand voice. Reference specific tool costs.",
      "acceptance_criteria": [
        "Post is under 200 words",
        "No banned words from brand-voice skill",
        "Starts with a hook line, not a link",
        "Ends with a question or CTA",
        "Saved to output/drafts/2026-02-04-linkedin-saas-vs-automation.md"
      ],
      "status": "pending"
    },
    {
      "id": "post-002",
      "title": "X Thread: Claude Code for Non-Devs",
      "description": "Write an X thread (max 5 posts) explaining how non-developers can use Claude Code. Conversational tone, no hashtags, no jargon.",
      "acceptance_criteria": [
        "Thread is 3-5 posts",
        "No hashtags",
        "No post exceeds 280 characters",
        "Saved to output/drafts/2026-02-04-x-claude-code-non-devs.md"
      ],
      "status": "pending"
    },
    {
      "id": "post-003",
      "title": "LinkedIn: Hooks Explained Simply",
      "description": "Write a LinkedIn post explaining Claude Code hooks to a non-technical audience. Use a kitchen analogy — hooks are like a timer that goes off automatically when your food is done.",
      "acceptance_criteria": [
        "Post is under 200 words",
        "Contains a relatable analogy",
        "No technical jargon",
        "Saved to output/drafts/2026-02-05-linkedin-hooks-explained.md"
      ],
      "status": "pending"
    },
    {
      "id": "post-004",
      "title": "IG Caption: AI Won't Replace You",
      "description": "Write an Instagram caption about how AI tools are assistants not replacements. Warm, direct tone. Positions automation as empowering.",
      "acceptance_criteria": [
        "Caption under 100 words",
        "3-5 hashtags at the end",
        "No emojis as bullet points",
        "Saved to output/drafts/2026-02-05-ig-ai-wont-replace-you.md"
      ],
      "status": "pending"
    },
    {
      "id": "post-005",
      "title": "LinkedIn: Repurpose from Blog",
      "description": "Read the blog post at /content/blog/n8n-automation-guide.md and repurpose it into a LinkedIn post. Change the angle — don't just shorten it.",
      "acceptance_criteria": [
        "Post is under 200 words",
        "Different angle from the original blog",
        "Standalone — makes sense without reading the blog",
        "Saved to output/drafts/2026-02-06-linkedin-n8n-repurposed.md"
      ],
      "status": "pending"
    }
  ]
}
```

**Run the autonomous loop**:
```
/ralph-loop "Work through the content brief in prd.json. For each story marked pending: write the post following the description and acceptance criteria, verify word count and banned words, save to output/drafts/, and mark the story complete. When all stories are done, output BATCH_DONE" --completion-promise "BATCH_DONE"
```

### Key Resources

- [Full video](https://www.youtube.com/watch?v=Y09u_S3w2c8)
- [Notion companion page](https://scrapeshq.notion.site/Every-Level-of-Claude-Code-Explained-in-39-Minutes-3007821711818048b119f78d5cc725ff)
- [Simon Scrapes Skool community](https://skool.com/scrapes)
- [GSD Framework](https://github.com/get-shit-done-cc) (referenced in video)
- [Ralph Loop / Ralph Wiggum plugin](https://github.com/anthropics/claude-code) (referenced in video)
- [Awesome MCP Servers](https://github.com/wong2/awesome-mcp-servers)
- [Community agents](https://github.com/wshobson/agents)
