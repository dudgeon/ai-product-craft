---
created: 2026-02-07
updated: 2026-02-07
template: templates/source.md
template_version: 1
tags: [source, ai-pm-craft, management, custom-gpts]
status: processed
source_type: article
source_url: "https://www.chatprd.ai/how-i-ai/scaling-yourself-as-a-manager-with-custom-gpts"
archive_url: "domains/professional-development/ai-pm-craft/sources/2026-02-07-hilary-gridley-scaling-yourself-custom-gpts.md"
author: "Claire Vo (interview with Hilary Gridley)"
published: 2025-05-19
discovered: 2026-02-07
domain: professional-development
project: ai-pm-craft
---

# Hilary Gridley's Playbook for Scaling Yourself with Custom GPTs

**By**: Claire Vo (ChatPRD) — interview with Hilary Gridley (Head of Core Product, WHOOP)
**Source**: [ChatPRD - How I AI](https://www.chatprd.ai/how-i-ai/scaling-yourself-as-a-manager-with-custom-gpts)
**Type**: article (podcast summary)

## Summary

Hilary Gridley demonstrates two ways to scale managerial expertise through AI. First, reverse-engineering your own implicit quality standards from before/after examples and encoding them into a custom GPT ("Deck Doctor") that delivers consistent, criteria-based feedback to your team. Second, using AI as a writing coach through a structured workflow: brain dump → thesis validation → blind spot detection → restructuring — where AI challenges and sharpens your thinking but you always do the final rewrite.

## Key Ideas Extracted

- **[[reverse-engineer-judgment-into-ai]]**: Collect before/after examples, have AI discover your implicit criteria, then encode into a reusable custom GPT
- **[[be-100x-more-specific]]**: Prompting technique that forces AI past vague principles into concrete, actionable standards — broadly applicable beyond the slide evaluation use case
- **[[my-job-your-job-role-delineation]]**: Explicit partitioning of human/AI responsibility in a prompt ("MY job is X, YOUR job is Y") — scopes AI authority, sets output format, preserves human agency
- **[[ai-as-writing-coach]]**: Structured workflow for using AI to sharpen written communication — thesis validation, blind spot detection, restructuring — where the human always writes the final version
- **[[scale-manager-expertise-with-ai]]**: Automate the "0-to-60%" repetitive feedback (slide reviews, writing coaching) so managers can focus on deep strategic thinking and personal mentorship

## Notes

The "be 100x more specific" prompt is deceptively powerful — it's a general-purpose technique for forcing AI past platitudes into actionable specifics. Works for any domain where you need concrete criteria.

The reverse-engineering approach is interesting because it starts open-ended intentionally — she doesn't want to bias the AI with her own framing first. Let AI discover patterns, then human refines. This is the opposite of most prompting advice ("be specific upfront").

The writing coach workflow embodies a key principle: use AI to *challenge* your thinking, not to *replace* it. The AI should help you "make it right" not "validate that it's right."

## Raw Content

Hilary Gridley, Head of Core Product at WHOOP, shares how she builds custom GPTs that clone her expert judgment to evaluate slide decks and uses AI as a writing coach to help her team's ideas go viral.

### Key Philosophy

The goal isn't to replace managers but to give them superpowers — automating repetitive feedback so you can spend time on deep strategic thinking and personal mentorship.

> "I kind of want the AI to start by interpreting this in ways that I might not even be able to predict. And then I'm gonna get an intune it and that's when I get super, super specific."

> "Try to get the AI to help you make it right as opposed to assuming that it's right and getting the AI to validate that."

### Workflow 1: Building a Custom GPT to Think and Evaluate Like You

The problem: as a manager, explaining what "good" looks like is hard. You know it when you see it, but turning intuition into clear, consistent feedback is a challenge.

**Step 1: Collect 'Good' and 'Bad' Examples**
- Two-column document of 'before' and 'after' slides
- Save as PDF — raw training data for AI to understand your taste

**Step 2: Reverse-Engineer Your Criteria with AI**
- Upload PDF to ChatGPT with intentionally simple, open-ended prompt (to avoid biasing the AI)
- AI analyzes before/after pairs and generates first-draft list of principles

**Step 3: Refine and Get Hyper-Specific**
- Key prompt: "Be 100 times more specific."
- Forces AI beyond vague principles into concrete, actionable standards
- Blend AI pattern-matching with your expert judgment

**Step 4: Build the 'Deck Doctor' GPT**
- Have the AI write GPT instructions: "MY job is to create a GPT that can evaluate slide decks... YOUR job is to write the prompt for it."
- AI generates detailed instructions including persona details
- Copy into GPT's 'Instructions' field

**Step 5: Test and Deploy with Your Team**
- Team members upload decks and get instant feedback based on your standards
- 1-5 rating on each criterion, concrete feedback, improvement suggestions
- Takes "0-to-60%" feedback off your plate

### Workflow 2: Using AI as a Writing Coach to Make Your Ideas Go Viral

Thesis: the best way to get invited to important strategic meetings is to be *pulled* in by writing up a strong point of view that gets shared around.

**Step 1: Brain Dump and Sanity Check**
- First draft, no filter
- "Can you succinctly express my thesis back to me and my main supporting points?"
- If AI can accurately summarize → on track. If not → clarify thinking first.

**Step 2: Make It More Compelling**
- "How can I make this more compelling?"
- AI as sparring partner — not rewriting, but expanding your thinking

**Step 3: Identify Blind Spots**
- "What blind spots might I have as I'm talking about this?"
- Flag: over-indexing on one user type, underplaying structural forces, false equivalences

**Step 4: Restructure for Clarity and Final Polish**
- Ask AI to suggest new structure
- Key principle: the process always ends with YOU
- Take all AI feedback → do the final rewrite yourself

### Takeaways for Managers

- Build expertise into custom GPTs → coaching tools that scale endlessly
- Use AI as writing partner → sharpen thinking, bigger impact
- Automate repetitive feedback → free yourself for deep strategic work
- The "be 100x more specific" technique is broadly applicable
