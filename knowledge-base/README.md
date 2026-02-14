---
created: 2026-02-08
updated: 2026-02-13
tags: [index, ai-pm-craft, knowledge-base]
status: active
domain: professional-development
project: ai-pm-craft
---

# Knowledge Map

Extracted knowledge organized by domain. Every entry traces back to one or more sources with quotes, context, and links. See `meta/taxonomy.md` for classification rules.

**Entry types**: `technique` · `mental-model` · `insight`
**Entry status**: `draft` → `solid` (multiple sources) → `canonical` (vetted, teachable)

---

## Product Lifecycle

Six phases. Entries sit flat within phase folders; the `component` frontmatter field records the most specific applicable component. See `meta/lifecycle-framework-v2.md` for full phase lineage and AI-PM emphasis.

### Discover

*What problems are worth solving?*
Components: Problem Signal Detection · Market & Competitive Intelligence · Opportunity Prioritization · Problem Brief

*No entries yet.*

### Frame

*What does success look like, and what's the bet?*
Components: Stakeholder Intent Alignment · Success Criteria & Business Case · Roadmap Definition

*No entries yet.*

### Shape

*What solution takes form, and for whom?*
Components: Persona & Journey Mapping · Prototyping & Risk Reduction · Go-to-Market Planning

- [Shape the Product — AI Disruption Profile](product-lifecycle/shape/shape-the-product-ai-disruption.md) — Determining what to build; most disrupted PM job (🤖🤖🤖), especially strategy/vision (🤖🤖🤖🤖)

### Build

*How do we ship with clarity and conviction?*
Components: Feature Specification Writing · User Story & Acceptance Criteria · Stakeholder Communication · Scope & Priority Tradeoffs

- [Interactive PRD Writing](product-lifecycle/build/interactive-prd-writing.md) — Templatized rule files + AI follow-up questions for thorough PRDs `build/feature-specification-writing`
- [Task List Generation for Observability](product-lifecycle/build/task-list-generation-for-observability.md) — Decomposing PRDs into nested task lists for observability and control `build/user-story-acceptance-criteria`
- [Context First Development](product-lifecycle/build/context-first-development.md) — The biggest mistake in AI-assisted dev is rushing past context `build`
- [Ship the Product — AI Disruption Profile](product-lifecycle/build/ship-the-product-ai-disruption.md) — Helping the team deliver; moderately disrupted (🤖🤖), scope tradeoffs remain human-driven

### Release

*How do we put this into the world deliberately?*
Components: Release Readiness Assessment · Phased Rollout Strategy · Release Communications · Launch Marketing & Enablement

*No entries yet.*

### Measure

*Did it work, and what do we do next?*
Components: KPI & Outcome Monitoring · Customer Feedback Collection · Experiment Design & Analysis · End-of-Life & Deprecation

*No entries yet.*

---

## Horizontal Domains

Knowledge areas that cut across the product lifecycle, organized by delivery mechanism with increasing capability and autonomy. See [taxonomy](../meta/taxonomy.md#horizontal-domains) for classification rules.

### [Context](horizontal/context/) — Knowledge Infrastructure

Making non-code knowledge discoverable and usable to agents and their human coworkers — context graphs, agent-oriented knowledge management, progressive disclosure.

- [Deliberate Context Selection](horizontal/context/deliberate-context-selection.md) — Hand-picking files for LLM context vs. relying on automatic context
- [Sync the People — AI Disruption Profile](horizontal/context/sync-the-people-ai-disruption.md) — Human coordination and alignment; least disrupted PM job (🤖), a durable competitive advantage

### [Prompting](horizontal/prompting/) — Portable Techniques

Portable techniques for crafting effective instructions — works in any chat window. Prompting patterns, writing workflows, role delineation.

- [Be 100x More Specific](horizontal/prompting/be-100x-more-specific.md) — Forces AI past vague principles into concrete, actionable standards
- [My Job Your Job Role Delineation](horizontal/prompting/my-job-your-job-role-delineation.md) — Explicit human/AI responsibility partitioning
- [AI as Writing Coach](horizontal/prompting/ai-as-writing-coach.md) — Structured workflow: thesis validation → blind spots → restructuring

### [Gems & GPTs](horizontal/gems-and-gpts/) — Packaged AI Tools

Packaged, shareable, non-agentic AI tools (Custom GPTs, Google Gems). Building and distributing for teams and organizations.

*No entries yet.*

### [Agents](horizontal/agents/) — Autonomous AI Participants

Filesystem-paired, autonomous agents — lifecycle management, rules, skills, templates. How PMs select, onboard, train, and performance-manage AI agents.

- [Stepwise Task Execution](horizontal/agents/stepwise-task-execution.md) — One-task-at-a-time execution with pause-and-approve checkpoints

## AI Adoption & Change Management

How organizations and individuals adapt to AI-native ways of working — scaling expertise, restructuring teams, driving adoption.

- [Reverse Engineer Judgment Into AI](ai-adoption/reverse-engineer-judgment-into-ai.md) — Have AI discover your implicit criteria, encode into reusable evaluator
- [Scale Manager Expertise With AI](ai-adoption/scale-manager-expertise-with-ai.md) — Automate "0-to-60%" feedback so managers focus on high-leverage work
- [AI Disrupts Strategic PM Skills Most](ai-adoption/ai-disrupts-strategic-pm-skills-most.md) — Counterintuitively, AI most disrupts high-level strategic PM skills, not soft skills

---

[← Back to AI PM Craft](../README.md)
