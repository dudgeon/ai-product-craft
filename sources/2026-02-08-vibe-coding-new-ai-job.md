---
title: "Getting Paid to Vibe Code: Inside the New AI-Era Job"
created: 2026-02-08
updated: 2026-02-14
template: templates/source.md
template_version: 3
tags: [source, ai-pm, vibe-coding, ai-coding, agent-workflows]
status: processed
source_type: podcast/newsletter
source_url: "https://www.lennysnewsletter.com/p/getting-paid-to-vibe-code"
archive_url: ""
author: "Lenny Rachitsky (with Lazar Jovanovic)"
published: 2026-02-08
discovered: 2026-02-08
summary: "Lazar Jovanovic, a full-time professional vibe coder at Lovable, breaks down how he ships production-quality products using only AI with no coding background. Covers PRD/markdown systems for agent alignment, parallel prototyping, 4x4 debugging workflow, and the convergence of product/engineering/design roles."
domain: professional-development
project: ai-pm
---

# Getting Paid to Vibe Code: Inside the New AI-Era Job

**By**: Lenny Rachitsky (with Lazar Jovanovic)
**Source**: [Lenny's Newsletter](https://www.lennysnewsletter.com/p/getting-paid-to-vibe-code)
**Type**: podcast/newsletter

## Summary

Lazar Jovanovic is a full-time professional vibe coder at Lovable. His job is to build both internal tools and customer-facing products purely using AI, while not having a coding background. Covers tactics, workflows, and frameworks for shipping production-quality products using only AI.

## Key Topics

1. Why having no coding background can be an advantage when building with AI
2. Why most of your time should go to planning and chat mode, not prompting
3. What to do when you get stuck: his 4x4 debugging workflow
4. The PRD and Markdown file system that keeps AI agents aligned across complex builds
5. Why kicking off four or five parallel prototypes is the best way to clarify your thinking
6. Why design skills and taste are going to be the most important skills in the future
7. His "genie and three wishes" mental model for making the most of AI's limitations
8. How product, engineering, and design roles are converging — and what that means for your career

## Key Ideas Extracted

- [Parallel Prototyping for Clarity](../knowledge-base/product-lifecycle/shape/parallel-prototyping-for-clarity.md) — Start 5 parallel builds with increasing specificity to explore the solution space
- [Structured Context Loading](../knowledge-base/horizontal/agents/system-design/structured-context-loading.md) — 4-file PRD system as structured context input for agent alignment
- [Context First Development](../knowledge-base/product-lifecycle/build/context-first-development.md) (enriched) — 80/20 planning-to-building ratio validates context-first as time allocation strategy
- [Deliberate Context Selection](../knowledge-base/horizontal/context/deliberate-context-selection.md) (enriched) — "Genie and three wishes" reframes context selection as resource allocation
- [Knowledge Capture as Side Effect](../knowledge-base/horizontal/agents/system-design/knowledge-capture-as-side-effect.md) (enriched) — Rules files as individual-practitioner version of the pattern

## Notes

Key takeaways to explore further:
- PRD/markdown systems for keeping AI agents aligned on complex builds
- 4x4 debugging workflow for problem-solving with AI
- Parallel prototyping approach (kicking off 4-5 prototypes to clarify thinking)
- The convergence of product/engineering/design roles
- Why design taste is becoming the critical skill vs. technical syntax knowledge
- "Genie and three wishes" mental model for working within AI limitations

Next steps:
- [ ] Extract key ideas into ai-pm knowledge base
- [ ] Consider how these workflows apply to work-agent-harness framework
- [ ] Review the Lovable PRD/base prompt generators referenced

## Raw Content

Lazar Jovanovic is Lovable's first full-time professional vibe coder — his job is building both internal tools and customer-facing products purely using AI, with no coding background. His work ranges from Shopify integrations and merch stores handling real transactions to complex internal dashboards tracking feature adoption. Companies across the S&P 500 are actively hiring people with these skills.

### Non-Technical Background as Advantage

People without engineering experience don't know what's "supposedly impossible," so they try things that technical people might dismiss. Lazar built Chrome extensions and desktop apps with Lovable because he didn't know the technical reasons why those shouldn't work. The willingness to try anything until proven wrong unlocks capabilities others overlook.

### 80/20 Planning-to-Building Ratio

Lazar spends 80% of his time planning and chatting with AI agents and only 20% building. The ceiling on AI output isn't model intelligence — it's what the model is told and shown before it acts. Your job is to provide clear context and instructions, not to write code.

### Context Window as Scarce Resource ("Genie and Three Wishes")

AI tools have a limited context window that you must manage deliberately. Think of it like a genie granting three wishes. Every request consumes tokens for reading, thinking, and executing. If you dump vague requests, the AI spends most tokens figuring out what you want and has little left for quality output.

### Parallel Prototyping for Clarity

Instead of overthinking one design, start five parallel builds: brain dump into the first project, get more specific in the second, add visual references in the third, attach actual code snippets in the fourth, and compare all five. This costs more up front but saves hundreds of credits and days of iteration later. Using AI to rapidly explore the solution space rather than committing to one path.

### Four-File PRD System for Agent Alignment

Create four PRD files before serious building begins:
1. **Master plan** — what and why
2. **Implementation plan** — sequence of work
3. **Design guidelines** — visual parameters
4. **User journeys** — how people navigate

These feed into a `tasks.md` file that breaks everything into executable steps. The agent reads these files before each prompt — a structured context loading system for non-agentic AI tools.

### 4x4 Debugging Workflow

When stuck, follow this four-step sequence:
1. Let the tool try to fix it
2. Add console logs to track what's happening, paste output back to the agent
3. Bring in an external tool (like Codex) for deeper diagnosis
4. Revert a few steps and try a cleaner prompt

### Rules Files as Cumulative Agent Training

After solving a problem, ask the AI how to prompt it better next time, then add that guidance to your `rules.md` file. The agent reads these rules on every request, so you're training it to handle your weaknesses automatically. Knowledge capture as a side effect of problem-solving.

### Design Taste as Differentiator

When everyone can produce good-enough output instantly, the people who stand out are those who understand emotional design decisions — fonts, spacing, micro-interactions — that AI can't yet replicate well. Invest time studying elite design work. Design skills and taste are becoming the most important skills, not technical syntax knowledge.

### Role Convergence

Product, engineering, and design roles are converging. Lazar's role didn't exist a year ago. The path to these jobs is building in public — shipping projects, teaching, sharing knowledge. Lovable hires submitted Lovable apps instead of resumes.

## Referenced Resources

- [Lovable](https://lovable.dev)
- [Lovable + Shopify](https://lovable.dev/shopify)
- [Mobbin](https://mobbin.com) — design reference
- [Dribbble](https://dribbble.com) — design reference
- [21st.dev](https://21st.dev)
- [Lovable base prompt generator](https://chatgpt.com/g/g-67e1da2c9c988191b52b61084438e8ee-lovable-base-prompt)
- [Lovable PRD generator](https://chatgpt.com/g/g-67e1e85fbeac8191a69b95c6d5c42ef6-lovable-prd-generator)
- [Felix Haas's newsletter (Design+AI)](https://designplusai.com)
- [UI style guide](http://uistyle.lovable.app)

## Related Episodes

- The new AI growth playbook for 2026: How Lovable hit $200M ARR in one year | Elena Verna
- Everyone's an engineer now: Inside v0's mission to create a hundred million builders | Guillermo Rauch
- The rise of Cursor: The $300M ARR AI tool that engineers can't stop using | Michael Truell
- The 100-person AI lab that became Anthropic and Google's secret weapon | Edwin Chen
- Why experts writing AI evals is creating the fastest-growing companies in history | Brendan Foody
