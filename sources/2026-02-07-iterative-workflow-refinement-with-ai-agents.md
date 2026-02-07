---
created: 2026-02-07
updated: 2026-02-07
template: templates/source.md
template_version: 2
tags: [source, ai-pm-craft]
status: unread
source_type: organic
source_url: ""
archive_url: "domains/professional-development/ai-pm-craft/sources/2026-02-07-iterative-workflow-refinement-with-ai-agents.md"
author: "Geoff Dudgeon and Claude"
published: 2026-02-07
discovered: 2026-02-07
summary: "Case study of iteratively refining an AI agent's skill file (rules governing source→knowledge extraction) over 3 rounds: decomposition guidance, portable prompting patterns, then ontology restructuring. Core thesis: the skill file is the real product — encode feedback as principles, not patches, so every future run benefits. Expect 3 passes; work at two levels (output + meta-rules) simultaneously."
domain: professional-development
project: ai-pm-craft
---

# Teaching an AI Agent to Think Like You: Iterative Workflow Refinement in Practice

**By**: Geoff Dudgeon and Claude
**Source**: Organic (user-authored draft)
**Type**: organic

## Summary

*Fill after reading.*

## Key Ideas Extracted

*Fill during processing.*

## Notes

*Draft organic source documenting the iterative refinement process used to build the ai-pm-craft knowledge base. Documents three rounds of feedback: decomposition guidance, portable prompting patterns, and ontology restructuring.*

## Raw Content

You've probably heard the advice: "Use AI to build workflows, not just answer questions." But what does that actually look like in practice? Not the polished version — the real version, with false starts, too-coarse first attempts, and the specific feedback that turns a mediocre AI collaboration into a genuinely useful one.

This post documents a real working session between a product manager and an AI coding agent (Claude Code). The goal was to build a personal knowledge management system for learning about AI product management. What emerged was a concrete example of something the industry is still figuring out: how to iteratively refine the *rules* an AI agent operates under, not just the outputs it produces.

---

## The Setup

The project is called "ai-pm-craft" — a structured learning system where external sources (articles, podcasts, newsletters) are read, processed, and decomposed into atomic knowledge entries. Think of it as a personal wiki with source lineage: every idea traces back to the specific quote and article that introduced it.

The system lives in a git repo as markdown files. The AI agent (Claude Code) has a skill file — a markdown document that defines *how* to process sources into knowledge entries. Here's what the initial skill file said about extracting ideas:

```markdown
**Atomicity matters.** One idea per knowledge entry. "This article
talks about three things" should produce three entries (or update
three existing ones), not one entry summarizing the article.
```

Simple enough. One idea per entry. Let's see what happened when we actually used it.

---

## Round 1: The Too-Coarse First Pass

The first source we processed was a podcast summary about Ryan Carson's three-step AI development playbook. Carson describes a system with three distinct phases:

1. **Generate a PRD** — using a rule file that instructs AI to ask clarifying questions
2. **Generate a task list** — decomposing the PRD into nested checkboxes
3. **Execute tasks one at a time** — with human approval between each step

The agent's first pass produced three knowledge entries:

- `prd-driven-ai-development` — lumped all three steps into one entry
- `context-first-development` — Carson's overarching "slow down to speed up" insight
- `deliberate-context-selection` — his Repo Prompt workflow for hand-picking LLM context

The problem was immediately obvious. `prd-driven-ai-development` was doing too much. It was three techniques wearing a trench coat pretending to be one. Each step has its own *why*, its own failure modes, its own situations where it applies or doesn't.

Here's the feedback that triggered the rewrite:

> Interactive PRD writing with (Ryan's core insight being templatization and the emphasis on follow-up questions), task list generation as mechanism to increase observability and control over agentic processes, plus increasing surface area to engage technical partners in the process, and task list processing — these are all discrete and important techniques that deserve their own entry.

Notice what's happening here. The human isn't saying "be more granular" in the abstract. He's identifying the specific *insight* in each technique that makes it independently valuable:

- Interactive PRD writing → the insight is **templatization** and **AI asking follow-up questions** (not just "write a PRD")
- Task list generation → the insight is **observability and stakeholder engagement surface** (not just "break things into tasks")
- Task list processing → the insight is **error containment through early detection** (not just "do tasks one at a time")

---

## The First Skill Update: Decomposition Guidance

Based on this feedback, the skill file was updated. The vague "atomicity matters" became concrete and prescriptive:

```markdown
**Atomicity matters — err on the side of more entries, not fewer.**
One idea per knowledge entry. If a source describes a three-step
workflow, each step is likely its own technique with its own
rationale and applicability. The test: does this step have its own
*why*, its own situations where it applies or doesn't, its own
nuances? If yes, it's a separate entry.

**Decompose workflows into their constituent techniques.** A
workflow like "PRD → Task List → Execution" contains three discrete
techniques: (1) interactive PRD writing (templatization + follow-up
questions), (2) task list generation (observability, stakeholder
engagement), (3) stepwise task execution (human-in-the-loop
checkpoints). Each has different value, different contexts where it
applies, and different lessons. Extract them separately.
```

Two new principles were also added:

```markdown
**Name entries by what they teach, not where they came from.**
"Ryan Carson's three-file system" is a source reference. "Interactive
PRD Writing with AI" is a teachable technique. The entry should be
recognizable and useful even if you've never read the source.

**Capture the unique mechanism, not just the outcome.** For a
technique, the *how* matters as much as the *what*. "Use AI to write
PRDs" is too vague. "Templatize PRD generation with rule files that
instruct AI to ask clarifying questions before writing" captures the
actual insight.
```

The agent then reprocessed the Carson source. The single `prd-driven-ai-development` entry was deleted and replaced with three focused entries, each with its own "How to Apply" section and its own context for when it's useful and when it's not.

---

## Round 2: Portable Prompting Patterns

With the Carson source properly decomposed, attention turned to the second processed source — a Hilary Gridley podcast about building custom GPTs. The agent had already extracted solid entries for the main workflows. But the human spotted something the agent missed:

> The "100x more specific" technique is a great find; it reminds me of her "my job/your job" pattern for prompt engineering, which also feels like something worth extracting.

Both of these are single steps embedded inside larger workflows. "Be 100 times more specific" is step 3 in a five-step process for building a custom GPT evaluator. "MY job is to create a GPT... YOUR job is to write the prompt for it" is step 4. But both are independently powerful — you could use either one tomorrow in a completely different context.

The feedback pointed to a category of knowledge entry the skill file didn't yet account for:

> ...and other insights of that level of specificity of the technique, but broad applicability of how it could be used. Please think about how to use this feedback to further refine the instruction-set.

This is the critical move: the human isn't just asking for a specific correction. He's asking the agent to *generalize the correction into a principle* that will prevent the same class of error in the future. The resulting skill update:

```markdown
**Watch for portable prompting patterns.** Some techniques are
embedded inside larger workflows but are independently valuable —
specific enough to use verbatim, broad enough to apply across many
contexts. Examples: "Be 100 times more specific" (forces AI past
platitudes in *any* domain), "MY job is X, YOUR job is Y" (delineates
human/AI responsibility in *any* prompt). These are easy to overlook
because they appear as single steps in a bigger workflow. Extract
them as their own entries whenever the mechanism is specific and the
applicability is broad. The test: could someone use this exact
pattern tomorrow in a completely different context and get value
from it?
```

---

## Round 3: The Ontology Shift

After two rounds of extraction refinement, the conversation moved up a level. The human looked at the Knowledge Map — the table of contents organizing all the knowledge entries — and realized the categories themselves were wrong:

> I think as we continue to refine this body of knowledge, there will be two broad categories: product lifecycle knowledge (e.g. PRD writing, interactive coding) vs horizontal (e.g. prompt engineering, working with agentic systems).

This isn't a correction to any individual entry. It's a structural insight about how the entries relate to each other. The original Knowledge Map was organized by PM function (Strategy, Execution, Measurement, UX, Technical Fluency, Stakeholder Dynamics, Career Growth). The new framing is two axes:

**Product Lifecycle** — knowledge organized by *stage of building a product*:
- Strategy & Vision
- Shipping & Execution
- Evaluation & Measurement
- User Experience & Design

**Horizontal Skills** — knowledge that applies *regardless of stage*:
- Prompt Engineering — specific patterns for getting better outputs from AI
- Working with Agentic Systems — the meta-process of building, evaluating, and refining human-AI collaboration

This distinction matters because it changes where things go. "Be 100x more specific" isn't about shipping or strategy — it's a prompting skill you use at every stage. "Context-first development" isn't about execution specifically — it's about how you work with agents in general.

---

## The Pattern: What Actually Happened

Step back and look at the whole arc:

1. **Goal-setting**: Define what we're building (a knowledge base with source lineage)
2. **Workflow creation**: Write a skill file that encodes how to process sources — on a spectrum from abstract principles ("atomicity matters") to concrete procedures ("create file, update index, update reading queue")
3. **Trial run**: Process two sources using the skill
4. **Evaluation**: Human reviews outputs, identifies specific quality gaps
5. **Rule refinement**: Update the skill file to encode the feedback as principles, not just fixes
6. **Reprocessing**: Re-run the same inputs through the updated rules
7. **Second evaluation**: Human reviews, spots another class of issue
8. **Second rule refinement**: Generalize the specific feedback into a reusable principle
9. **Ontology revision**: Step up a level and restructure the categories themselves

This is not "prompting." It's something more like *collaborative system design* — where the human and the agent are iteratively building the rules that govern the agent's future behavior. Each round of feedback doesn't just fix the current output; it improves every future output by refining the system.

A few things are notable about this process:

**The feedback is about principles, not patches.** When the human says "these should be separate entries," the agent doesn't just split that one entry — it adds a decomposition principle to the skill file that applies to all future sources. When the human spots a missed portable pattern, the agent doesn't just add the entry — it creates a "watch for portable patterns" principle.

**The skill file is the real product.** The knowledge entries are valuable, but the skill file — the rules for *how to produce* knowledge entries — is what compounds. After three rounds, the skill file went from one vague principle ("atomicity matters") to five specific, actionable principles with concrete examples. Every future source processed by this agent benefits from all three rounds of feedback.

**The human contributes judgment; the agent contributes coverage and consistency.** The human spots "these are different techniques" and "this pattern is portable." The agent operationalizes those insights into rules, reprocesses existing work, updates all cross-references, and ensures everything is consistent. Neither could do the other's job well.

---

## What This Means for PMs

If you're a product manager working with AI tools, this iterative refinement pattern is worth internalizing:

**Don't optimize prompts. Build systems.** A prompt is a one-shot instruction. A skill file (or system prompt, or rule set, or custom instructions) is a reusable system that encodes your accumulated judgment. The first version will be too vague. That's fine — the point is to have a *place* to encode refinements as you discover them.

**Your feedback is the training data.** Every time you look at AI output and say "that's too coarse" or "you missed this pattern," you're generating a training signal. But most people discard that signal — they fix the output and move on. The leverage move is to *encode the feedback into the rules* so the AI gets it right by default next time.

**Expect three passes.** In our experience, the first pass is always too coarse. The second pass gets the granularity right but misses cross-cutting patterns. The third pass restructures the categories. Plan for this. Don't treat the first output as final.

**Work at two levels simultaneously.** There's the work itself (processing sources, writing entries) and the meta-work (refining the rules that govern how work gets done). The meta-work compounds. An hour spent improving the skill file saves ten hours across future processing runs.

---

## Appendix: The Skill File Evolution

For reference, here's how the key section of the skill file evolved across three rounds:

**Version 1** (initial):
```markdown
Atomicity matters. One idea per knowledge entry.
```

**Version 2** (after first feedback):
```markdown
Atomicity matters — err on the side of more entries, not fewer.

Decompose workflows into their constituent techniques.

Name entries by what they teach, not where they came from.

Capture the unique mechanism, not just the outcome.
```

**Version 3** (after second feedback):
```markdown
Watch for portable prompting patterns. Some techniques are embedded
inside larger workflows but are independently valuable — specific
enough to use verbatim, broad enough to apply across many contexts.
```

**Version 4** (after ontology revision):
```markdown
Knowledge Map Sections — Two axes:

Product Lifecycle (vertical): Strategy & Vision, Shipping &
Execution, Evaluation & Measurement, UX & Design

Horizontal Skills (cut across lifecycle stages): Prompt Engineering,
Working with Agentic Systems
```

Each version didn't replace the previous one — it *added a layer* of specificity. The skill file accumulated judgment over time, just like the knowledge base it governs.
