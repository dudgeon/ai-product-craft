---
created: 2026-02-08
updated: 2026-02-13
tags: [meta, ai-pm-craft, taxonomy]
status: active
---

# AI PM Craft — Taxonomy

Canonical reference for classifying knowledge entries. Used by the source processing skill and knowledge entry template.

For full phase lineage, component descriptions, and AI-PM emphasis, see [Lifecycle Framework V2](lifecycle-framework-v2.md).

---

## Three Domains

Every knowledge entry belongs to exactly one domain.

| Domain | Folder | What belongs here |
|---|---|---|
| **Product Lifecycle** | `knowledge-base/product-lifecycle/{phase}/` | Techniques and insights that augment a specific stage of building product |
| **Horizontal** | `knowledge-base/horizontal/{horizontal_domain}/` | Knowledge areas and practices that cut across the lifecycle — see Horizontal Domains below |
| **AI Adoption** | `knowledge-base/ai-adoption/` | How organizations and individuals adapt to AI-native ways of working — scaling expertise, org change, driving adoption |

### Classification test

1. **Does this technique augment a specific lifecycle phase?** → Product Lifecycle (file under the phase)
2. **Is it a cross-cutting skill, methodology, or knowledge area?** → Horizontal (then determine which horizontal domain — see below)
3. **Is it about bringing others along or changing how teams/orgs work?** → AI Adoption

---

## Horizontal Domains

The horizontal domain is organized as a stack by delivery mechanism, with increasing capability and autonomy. Each layer is a knowledge area with its own depth. Entries sit flat in their horizontal domain folder; the `horizontal_domain` frontmatter field records which one.

| Horizontal Domain | Slug | Folder | What belongs here |
|---|---|---|---|
| **Context** | `context` | `horizontal/context/` | Knowledge infrastructure: making non-code knowledge discoverable and usable to agents and their human coworkers — context graphs, agent-oriented KM, progressive disclosure, knowledge discoverability. |
| **Prompting** | `prompting` | `horizontal/prompting/` | Portable techniques for crafting effective instructions — works in any chat window. Prompting patterns, writing workflows, role delineation, refinement techniques. |
| **Gems & GPTs** | `gems-and-gpts` | `horizontal/gems-and-gpts/` | Packaged, shareable, non-agentic AI tools (Custom GPTs, Google Gems). Building, distributing, and managing for teams and organizations. Key differentiator: distributable. |
| **Agents** | `agents` | `horizontal/agents/` | Filesystem-paired, autonomous agents — lifecycle management, rules, skills, templates. How PMs select, onboard, train, give feedback to, and performance-manage AI agents. |

### Horizontal classification test

1. **Is it about making knowledge discoverable and usable?** → Context
2. **Is it a portable prompting technique (works in any chat window)?** → Prompting
3. **Is it about packaged, shareable, non-agentic AI tools?** → Gems & GPTs
4. **Is it about autonomous, filesystem-paired agents?** → Agents

### Dual attribution

Horizontal entries frequently relate to specific lifecycle phases. Use `lifecycle_phase` in frontmatter (optional for horizontal entries) to record the primary phase connection when one exists. An entry about how deliberate context selection improves PRD writing would live in Context with `lifecycle_phase: build` as a cross-reference. **One idea can be attributed to multiple domains** — when an insight genuinely belongs in both a horizontal domain and a lifecycle phase, create the entry where it has the most depth and add cross-references via the Related section.

---

## Product Lifecycle Phases

Six phases, each with named components. Entries sit flat in the phase folder; the `component` frontmatter field records the most specific applicable component.

### 1. Discover

*What problems are worth solving?*

| Component | Slug | Description |
|---|---|---|
| Problem Signal Detection | `problem-signal-detection` | Detecting unmet needs from data, support, sales, and customer contact |
| Market & Competitive Intelligence | `market-competitive-intelligence` | Competitive analysis, market sizing, trend monitoring |
| Opportunity Prioritization | `opportunity-prioritization` | Ranking and managing the space of possible problems |
| Problem Brief | `problem-brief` | Concise articulation of the problem, who it affects, why now |

### 2. Frame

*What does success look like, and what's the bet?*

| Component | Slug | Description |
|---|---|---|
| Stakeholder Intent Alignment | `stakeholder-intent-alignment` | Refining intent, securing sponsorship, shared understanding |
| Success Criteria & Business Case | `success-criteria-business-case` | KPIs, financial modeling, defining the objective function |
| Roadmap Definition | `roadmap-definition` | Outcome-based roadmapping, strategic sequencing, scoping |

### 3. Shape

*What solution takes form, and for whom?*

| Component | Slug | Description |
|---|---|---|
| Persona & Journey Mapping | `persona-journey-mapping` | User models, behavioral archetypes, JTBD framing |
| Prototyping & Risk Reduction | `prototyping-risk-reduction` | Wireframes, prototypes, fat-marker sketches, assumption testing |
| Go-to-Market Planning | `gtm-planning` | Positioning, messaging, channel strategy, pricing |

### 4. Build

*How do we ship with clarity and conviction?*

| Component | Slug | Description |
|---|---|---|
| Feature Specification Writing | `feature-specification-writing` | PRDs, specs, technical design documents |
| User Story & Acceptance Criteria | `user-story-acceptance-criteria` | Story decomposition, acceptance criteria, story mapping |
| Stakeholder Communication | `stakeholder-communication` | Status updates, cross-functional coordination, expectation management |
| Scope & Priority Tradeoffs | `scope-priority-tradeoffs` | Scope negotiations, circuit breakers, quality/speed tradeoffs |

### 5. Release

*How do we put this into the world deliberately?*

| Component | Slug | Description |
|---|---|---|
| Release Readiness Assessment | `release-readiness-assessment` | Go/no-go evaluation, quality gates, support readiness |
| Phased Rollout Strategy | `phased-rollout-strategy` | Feature flags, canary deploys, segment-based rollouts |
| Release Communications | `release-communications` | Changelogs, release notes, stakeholder notifications |
| Launch Marketing & Enablement | `launch-marketing-enablement` | Launch campaigns, sales enablement, customer success briefings |

### 6. Measure

*Did it work, and what do we do next?*

| Component | Slug | Description |
|---|---|---|
| KPI & Outcome Monitoring | `kpi-outcome-monitoring` | North Star dashboards, OKR reviews, post-launch accountability |
| Customer Feedback Collection | `customer-feedback-collection` | NPS/CSAT, surveys, support themes, interview programs |
| Experiment Design & Analysis | `experiment-design-analysis` | A/B tests, statistical rigor, acting on results |
| End-of-Life & Deprecation | `end-of-life-deprecation` | Sunsetting, migration paths, deprecation communication |

---

## Entry Types

| Type | Slug | What it captures |
|---|---|---|
| Technique | `technique` | A named method, practice, or procedure |
| Mental Model | `mental-model` | A framework for thinking about a class of problems |
| Insight | `insight` | An observation, principle, or non-obvious pattern |

## Entry Status

| Status | Meaning | Promotion criteria |
|---|---|---|
| `draft` | Initial capture from one source | — |
| `solid` | Supported by multiple sources, well-articulated | Corroboration from a second independent source |
| `canonical` | Thoroughly vetted, teachable | Could teach this to someone; no open questions |

## Entry Origin

| Origin | Meaning |
|---|---|
| `sourced` | Extracted from external sources |
| `organic` | From personal experience |
| `both` | Originated organically, later found external validation |

---

## Frontmatter Reference

Knowledge entry frontmatter fields for taxonomy:

```yaml
# Required
entry_type: technique | mental-model | insight
domain: product-lifecycle | horizontal | ai-adoption

# Required for product-lifecycle entries
lifecycle_phase: discover | frame | shape | build | release | measure
component: <component-slug from tables above>

# Required for horizontal entries
horizontal_domain: context | prompting | gems-and-gpts | agents

# Optional for horizontal entries (dual attribution)
lifecycle_phase: discover | frame | shape | build | release | measure  # when the entry has a primary phase connection

# Optional
featured: true  # Worth championing organizationally
```

---

## Placement Rules

1. **Most specific component wins.** If an entry clearly maps to a lifecycle component, tag it there. If it spans multiple components within a phase, use the primary one and note connections in Related.
2. **Phase-level is OK.** If an entry fits a phase but not a specific component, omit the `component` field and file it in the phase folder.
3. **Cross-phase entries go horizontal.** If an entry applies across 3+ phases, it's probably a horizontal entry. Determine which horizontal domain fits best.
4. **Horizontal domain entries can reference lifecycle phases.** Use `lifecycle_phase` in frontmatter to record the primary phase connection when one exists. Use the Related section to cross-reference entries in other domains.
5. **Match to delivery mechanism.** A portable prompting technique → Prompting. Knowledge infrastructure → Context. A packaged, shareable tool → Gems & GPTs. Autonomous agent management → Agents.
6. **When in doubt, ask.** Don't force-fit entries into the taxonomy. Flag uncertain placements for review.
7. **Screen for adoption.** Sources often embed change management insights alongside craft techniques. Extract these separately into ai-adoption.
8. **Screen for horizontal domain insights.** Sources about delivery workflows may contain agent management insights or knowledge management patterns. Extract these into the appropriate horizontal domain.
