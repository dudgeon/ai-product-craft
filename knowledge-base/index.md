---
created: 2026-02-08
updated: 2026-02-19
tags: [index, ai-pm, knowledge-base]
status: active
domain: professional-development
project: ai-pm
---

# Knowledge Map

![Product Lifecycle Map](product-lifecycle-map.png)

Extracted knowledge organized by domain. Every entry traces back to one or more sources with quotes, context, and links. See `meta/taxonomy.md` for classification rules.

**Entry types**: `technique` · `mental-model` · `insight`
**Entry status**: `draft` → `solid` (multiple sources) → `canonical` (vetted, teachable)

---

## Product Lifecycle

Six phases. Entries sit flat within phase folders; the `component` frontmatter field records the most specific applicable component. See `meta/lifecycle-framework-v2.md` for full phase lineage and AI-PM emphasis.

### Discover

*What problems are worth solving?*
Components: Problem Signal Detection · Market & Competitive Intelligence · Opportunity Prioritization · Problem Brief

- [Quote Selection Rules for AI Analysis](product-lifecycle/discover/quote-selection-rules-for-ai-analysis.md) — Define explicit quote rules before AI extraction to prevent generation of plausible-sounding paraphrases `discover/problem-signal-detection`
- [Quote Verification Pass](product-lifecycle/discover/quote-verification-pass.md) — Dedicated follow-up prompt to confirm each extracted quote exists verbatim in the source `discover/problem-signal-detection`
- [Decision-Anchored Analysis Context](product-lifecycle/discover/decision-anchored-analysis-context.md) — 4-component context loading (project context, business goal, product context, participant overview) to anchor AI analysis to your specific decision `discover/problem-signal-detection`
- [Few-Shot Calibration for Analysis Classification](product-lifecycle/discover/few-shot-calibration-for-analysis.md) — Labeled examples with rationale for each category level; examples teach, descriptions don't `discover/problem-signal-detection`
- [AI Analysis Multi-Pass Verification](product-lifecycle/discover/ai-analysis-multi-pass-verification.md) — Deliberate second pass targeting quote errors, within-participant contradictions, and thin evidence `discover/problem-signal-detection`
- [Latent Demand as Product Signal](product-lifecycle/discover/latent-demand-as-product-signal.md) — Find what people are already doing despite friction; observed off-label behavior reveals unmet demand before any ideation effort `discover/problem-signal-detection`

### Frame

*What does success look like, and what's the bet?*
Components: Stakeholder Intent Alignment · Success Criteria & Business Case · Roadmap Definition

*No entries yet.*

### Shape

*What solution takes form, and for whom?*
Components: Persona & Journey Mapping · Prototyping & Risk Reduction · Go-to-Market Planning

- [Shape the Product — AI Disruption Profile](product-lifecycle/shape/shape-the-product-ai-disruption.md) — Determining what to build; most disrupted PM job (🤖🤖🤖), especially strategy/vision (🤖🤖🤖🤖)
- [Parallel Prototyping for Clarity](product-lifecycle/shape/parallel-prototyping-for-clarity.md) — Start 5 parallel builds with increasing specificity; AI makes prototyping cheap enough to explore broadly before converging

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

Lifecycle-agnostic AI PM skills and knowledge areas, organized by delivery mechanism with increasing capability and autonomy. See [taxonomy](../meta/taxonomy.md#horizontal-domains) for classification rules.

### [Prompting](horizontal/prompting/) — Portable Techniques

Portable techniques for crafting effective instructions — works in any chat window. Prompting patterns, meta-skill patterns, writing workflows, role delineation.

- [Be 100x More Specific](horizontal/prompting/be-100x-more-specific.md) — Forces AI past vague principles into concrete, actionable standards
- [My Job Your Job Role Delineation](horizontal/prompting/my-job-your-job-role-delineation.md) — Explicit human/AI responsibility partitioning
- [AI as Writing Coach](horizontal/prompting/ai-as-writing-coach.md) — Structured workflow: thesis validation → blind spots → restructuring
- [LLMs Generate, Not Retrieve](horizontal/prompting/llms-generate-not-retrieve.md) — Root cause mental model: LLMs produce statistically plausible text, not retrieved text; explains hallucinated quotes, fabricated citations, confident errors

### [Context & Knowledge Management](horizontal/context/) — Knowledge Infrastructure

Making non-code knowledge discoverable and usable to agents and their human coworkers — context graphs, agent-oriented knowledge management, progressive disclosure.

- [Deliberate Context Selection](horizontal/context/deliberate-context-selection.md) — Hand-picking files for LLM context vs. relying on automatic context
- [Sync the People — AI Disruption Profile](horizontal/context/sync-the-people-ai-disruption.md) — Human coordination and alignment; least disrupted PM job (🤖), a durable competitive advantage
- [Three-Layer Context Disclosure](horizontal/context/three-layer-context-disclosure.md) — Index → summary → full content: the converging pattern for efficient agent retrieval (~10x token savings)
- [Filesystem as Retrieval Architecture](horizontal/context/filesystem-as-retrieval-architecture.md) — Directory hierarchy as index, frontmatter as metadata, git as temporal layer — a legitimate retrieval system, not a stopgap
- [Repositories as Context Boundaries](horizontal/context/repositories-as-context-boundaries.md) — Repos shift from code isolation to context containers; git subtree/submodules as cross-repo context distribution; agents absorb submodule ceremony
- [Agent-Self-Managed Progressive Disclosure](horizontal/context/agent-self-managed-progressive-disclosure.md) — Agents actively reorganize their own memory filesystem: filetree as navigation signal, frontmatter as preview, system/ for always-loaded; dynamic not static disclosure

### [Templated AI Runtimes](horizontal/runtimes/) — Packaged AI Tools

Packaged, shareable, non-agentic AI tools (Custom GPTs, Google Gems, Claude Projects). Building, distributing, and managing templated AI runtimes for teams and organizations.

*No entries yet.*

### [Agents](horizontal/agents/) — Building & Managing Knowledge Agents

Building and managing knowledge agents — lifecycle management, rules, skills, templates, tools, workflows. How PMs select, onboard, train, and performance-manage AI agents.

#### [System Design](horizontal/agents/system-design/) — Agent System Design

**[Instruction Design](horizontal/agents/system-design/instruction-design/)** — CLAUDE.md, agents.md & behavioral configuration
- [Structured Context Loading](horizontal/agents/system-design/instruction-design/structured-context-loading.md) — Purpose-built files loaded before each interaction to align agent behavior
- [Knowledge Capture as Side Effect](horizontal/agents/system-design/instruction-design/knowledge-capture-as-side-effect.md) — Design agent systems so knowledge capture is a byproduct of corrections `solid`

**[Skills](horizontal/agents/system-design/skills/)** — Discrete agent capabilities
- [Meta-Skill Pattern](horizontal/agents/system-design/skills/meta-skill-pattern.md) — Build a "skill that builds skills" to bootstrap agent capabilities consistently
- [Agent Memory Lifecycle Skills](horizontal/agents/system-design/skills/agent-memory-lifecycle-skills.md) — Initialize (bootstrap from history), Reflect (sleep-time synthesis), Defragment (reorganize to 15–25 files) as the three built-in skills for maintaining agent memory health

**[Supervision](horizontal/agents/system-design/supervision/)** — Human governance of agent execution
- [Stepwise Task Execution](horizontal/agents/system-design/supervision/stepwise-task-execution.md) — One-task-at-a-time execution with pause-and-approve checkpoints
- [Progressive Tool Disclosure](horizontal/agents/system-design/supervision/progressive-tool-disclosure.md) — Revealing MCP tools in layers to combat choice paralysis and hallucination (+15% accuracy)
- [Agent-Mediated Self-Reflection](horizontal/agents/system-design/supervision/agent-mediated-self-reflection.md) — Using agents to observe behavioral patterns from digital exhaust

**[Architecture](horizontal/agents/system-design/architecture/)** — Structural foundations
- [Filesystem as Agent State](horizontal/agents/system-design/architecture/filesystem-as-agent-state.md) — Agent architecture = filesystem (state) + LLM (orchestrator); company-as-filesystem
- [Agent as Cross-Tool Workflow Hub](horizontal/agents/system-design/architecture/agent-as-cross-tool-workflow-hub.md) — Local agent + MCP integrations as orchestration layer across disconnected SaaS tools
- [Git-Versioned Agent Memory](horizontal/agents/system-design/architecture/git-versioned-agent-memory.md) — Every memory change is a commit with message; audit trail, rollback, temporal narrative of agent learning; extends filesystem-as-retrieval with a temporal layer
- [Concurrent Agent Memory via Git Worktrees](horizontal/agents/system-design/architecture/concurrent-agent-memory-via-worktrees.md) — Multiple subagents write to shared memory simultaneously via isolated git worktrees; enables memory swarms for initialization and parallel learning

#### [Harnesses](horizontal/agents/harnesses/) — Platform-Specific Knowledge

- [Cursor: Structured AI Development](horizontal/agents/harnesses/cursor-structured-ai-development.md) — Three-file rule system, @-includes, MCP config, and Repo Prompt for structured workflows in Cursor
- [Plan Mode as Claude Code Default](horizontal/agents/harnesses/plan-mode-as-claude-code-default.md) — Begin 80% of tasks in plan mode ("don't write code yet"); review plan, then auto-accept for near-certain one-shot implementation with Opus 4.6

#### [Managing Agents](horizontal/agents/managing-agents/) — The Human-Agent Management Relationship

The practice of managing AI agents as autonomous participants. Distinct from system design (building agents) and harnesses (platforms) — this is about the *relationship* between human and agent.

**Thesis**: [Talent-to-Direction Scarcity Shift](horizontal/agents/managing-agents/talent-to-direction-scarcity-shift.md) — AI inverts traditional scarcity: talent is abundant, knowing what to ask for is the bottleneck

**Task-Agent Fit**:
- [Delegation Decision Framework](horizontal/agents/managing-agents/task-fit/delegation-decision-framework.md) — Three-variable equation (Human Baseline Time × Probability of Success × AI Process Time) for when delegation pays off

**Delegation Craft**:
- [Delegation Documentation as Agent Prompts](horizontal/agents/managing-agents/delegation/delegation-documentation-as-prompts.md) — Every field's delegation docs (PRDs, shot lists, Five Paragraph Orders) are AI prompts; common elements pattern

**Agent Selection & Onboarding**:
- [Model Fit for Qualitative Analysis Tasks](horizontal/agents/managing-agents/selection/model-fit-for-qualitative-analysis.md) — Claude (depth/breadth), Gemini (evidenced themes), ChatGPT (stakeholder framing) as distinct strengths for analysis work; technique quality matters more than model choice
- [Capability Over Cost in Model Selection](horizontal/agents/managing-agents/selection/capability-over-cost-in-model-selection.md) — Use max-capable model, not cheapest; smarter models burn fewer tokens overall vs. cheap models correcting their own mistakes

## AI Adoption & Change Management

How organizations and individuals adapt to AI-native ways of working — scaling expertise, restructuring teams, driving adoption.

- [Reverse Engineer Judgment Into AI](ai-adoption/reverse-engineer-judgment-into-ai.md) — Have AI discover your implicit criteria, encode into reusable evaluator
- [Scale Manager Expertise With AI](ai-adoption/scale-manager-expertise-with-ai.md) — Automate "0-to-60%" feedback so managers focus on high-leverage work
- [AI Disrupts Strategic PM Skills Most](ai-adoption/ai-disrupts-strategic-pm-skills-most.md) — Counterintuitively, AI most disrupts high-level strategic PM skills, not soft skills
- [Data Silos Block Enterprise Agent Adoption](ai-adoption/data-silos-block-agent-adoption.md) — Enterprise data fragmented across SaaS tools is the primary barrier to agent rollout, not model capability
- [Tool Identity as Adoption Gate](ai-adoption/tool-identity-as-adoption-gate.md) — When a capable AI tool has narrow adoption, the bottleneck may be naming/branding/positioning, not capability
- [Retrieval Infrastructure Graduation](ai-adoption/retrieval-infrastructure-graduation.md) — Tiered path from filesystem-only → semantic search → knowledge graph, with graduation criteria for each transition
- [Raise the Floor vs Raise the Ceiling](ai-adoption/raise-the-floor-vs-raise-the-ceiling.md) — Two axes of AI adoption: floor (Gems, packaged runtimes for everyone) vs ceiling (agentic methods for power users); effective change management sequences and balances both
- [Build for Future Model Capability](ai-adoption/build-for-future-model-capability.md) — Design AI products for the model 6 months out, not today; accept poor early PMF as the cost of being ready when that model ships
- [Intentional Understaffing for AI-First Teams](ai-adoption/intentional-understaffing-ai-first-teams.md) — Deliberately staff lightly to force AI to carry more work; constraint drives creative AI adoption, not just faster typing
- [Delay Token Cost Optimization](ai-adoption/delay-token-cost-optimization.md) — Give teams unlimited tokens during experimentation; token cost < salary cost at small scale; optimize only after proven scale
- [Generalists Outperform Specialists in AI Era](ai-adoption/generalists-outperform-specialists-ai-era.md) — AI compresses deep execution; curious cross-discipline generalists capture the highest rewards as AI handles more of the specialist's edge

---

## Adjacent Disciplines

How AI transforms the disciplines of PMs' close collaborators (engineering, design, analytics) — and what their shifting AI adoption means for product leadership. In many non-AI-native orgs, engineering leads product in agentic adoption; PMs are likely to lead design and analytics.

- [Spec-Driven Development](adjacent-disciplines/spec-driven-development.md) — Software ships as specs + tests with zero code; works for stable utilities, breaks for anything needing performance, debugging, community, or security patching
- [AI Moves from Execution to Ideation](adjacent-disciplines/ai-moves-from-execution-to-ideation.md) — AI is beginning to generate product ideas from telemetry and feedback, not just execute instructions; engineering shifts from implementation to judgment curation

---

[← Back to AI PM](../)
