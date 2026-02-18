---
title: "Scaling People → Scaling Agents"
created: 2026-02-09
updated: 2026-02-09
template: templates/source.md
template_version: 3
tags: [source, ai-pm]
status: unread
source_type: organic
source_url: ""
archive_url: ""
author: "Geoff Dudgeon, Claude Opus 4.6"
published:
discovered: 2026-02-09
summary: "Maps Claire Hughes Johnson's Scaling People management framework to AI agent management with high fidelity. Introduces five-mechanism layer (rules, skills, tools, workflows, context), retro pattern as core management loop, trust tiers with graduation, skill-reliability matrix, delegation cube (impact × reversibility × mechanism maturity), and attention economics. Argues agent management requires by default the codification CHJ spent 480 pages advocating — the forced-explicit irony."
domain: professional-development
project: ai-pm
---

# Scaling People → Scaling Agents

**By**: Geoff Dudgeon, Claude Opus 4.6
**Type**: organic

## Summary

A comprehensive framework that adapts Claire Hughes Johnson's *Scaling People* — her practitioner's handbook for management at Google and Stripe — to the management of AI agents. The thesis: the same disciplines that make someone a good manager of people (self-awareness, clear communication, structured feedback, principled delegation, rigorous evaluation) are substantially the same skills that make someone effective at managing agents. The framework introduces the "mechanism layer" (rules, skills, tools, workflows, context) as the infrastructure through which agent behavior is shaped, and the "retro pattern" as the core management loop that drives continuous improvement. Key concepts include trust tiers with graduation, the skill-reliability matrix, the delegation cube, layer-specific diagnosis, and attention economics.

## Key Ideas Extracted

*Awaiting processing.*

## Notes

Draft v4. Substantial organic work — 15 named concepts in the key concepts index. This is the densest single source in the knowledge base and will likely produce the most knowledge entries of any source when processed. Many concepts map directly to the horizontal/agents domain; some (like attention economics and the forced-explicit irony) are broader insights that may land in ai-adoption.

The document explicitly references and builds on CHJ's *Scaling People* as the source text, but the agent-management adaptation is original work.

## Raw Content

**Geoff Dudgeon and Claude Opus 4.6 · 2026 · Organic**

### The Source Material

Claire Hughes Johnson was Chief Operating Officer at Stripe from 2014 to 2021, a period in which the company grew from roughly 200 employees to more than 8,000. Before that, she spent a decade at Google leading teams across Gmail, Google Apps, AdWords, and the self-driving car project. In 2023, she published *Scaling People: Tactics for Management and Company Building* — a practitioner's handbook for how to actually run a high-growth organization, drawn from nearly two decades of operating at the highest levels of two generational companies.

The book is organized around four operating principles and four core frameworks:

**Operating Principles:**

1. Build self-awareness to build mutual awareness
2. Say the thing you think you cannot say
3. Distinguish between management and leadership
4. Come back to your operating system

**Core Frameworks:**

1. Foundations and planning — founding documents, goals, metrics, operating cadence
2. Hiring — recruiting pipelines, structured interviews, onboarding
3. Team development — structuring teams, delegation, meetings, reorgs
4. Feedback and performance — coaching, formal reviews, calibration, managing high and low performers

What makes *Scaling People* distinctive is its insistence on making the implicit explicit. Hughes Johnson argues, chapter after chapter, that the companies that scale successfully are the ones that codify their mission, write down their values, document their operating systems, formalize their feedback processes, and build repeatable structures that allow people to do their best work. The alternative — relying on tribal knowledge, unwritten norms, and the charisma of founders — breaks down reliably somewhere between 50 and 500 employees.

This emphasis on codification turns out to be prophetic in ways Hughes Johnson likely didn't intend.

---

### The Pivot

Leaders increasingly gain leverage not just through human teammates, but through a growing number and variety of semi-autonomous agents. A product manager who once relied on a team of analysts, writers, and researchers now also relies on AI agents to draft documents, synthesize research, generate code, analyze data, and manage workflows. The number and diversity of these agents will only increase.

These agents require management. Not metaphorically — literally. They need to be selected for specific roles. They need to be onboarded with the right context. They need clear goals and success criteria. They need ongoing feedback to improve. Their performance needs to be evaluated. Their scope needs to expand or contract based on demonstrated capability. And the information worker who does this well will dramatically outperform the one who doesn't.

The thesis of this document is straightforward: the management frameworks Hughes Johnson developed for scaling human organizations apply, with real fidelity, to the management of AI agents. The skills that make someone a good manager of people — self-awareness, clear communication, structured feedback, principled delegation, rigorous evaluation — are substantially the same skills that make someone effective at managing agents.

This is not to say agents are people. The analogy has limits, and we'll address those. But the practical overlap is large enough, and specific enough, to be genuinely useful as a framework.

#### What We Mean by "Agent"

An agent, for our purposes, is an AI system that can take action toward a goal with some degree of autonomy. This ranges from a simple chat interaction ("summarize this document") to a complex multi-step workflow ("research these five companies, build a comparison matrix, draft a recommendation memo, and save it to my project folder"). The defining characteristic is that the agent exercises judgment about *how* to accomplish a task, not just *whether* to execute a fixed instruction.

Agents vary in capability, autonomy, and specialization. Some are general-purpose (a Claude conversation). Some are specialized (a coding agent, a research agent with web access, a data analysis agent). Some operate in isolation; others are orchestrated into ensembles where the output of one feeds the input of another.

#### The Five Steering Mechanisms

Beyond selecting a base model, the information worker has five mechanisms to shape how an agent behaves. These are not abstractions. In current agent environments — Claude's project system, Windsurf, Cursor, Claude Code, and similar tools — each of these mechanisms corresponds to something concrete: a file you can read, a setting you can change, a document you can share with a colleague. No engineering or data science background is required.

**Rules** — Persistent behavioral guidelines that shape how an agent thinks and acts. Rules encode values, preferences, constraints, self-knowledge, and operating principles. They are the agent's equivalent of internalized culture and personal norms. In practice, rules are plain-language statements that you write in a rules file or project instructions: "Default to concise output unless the user requests detail," or "When asked about tax implications, flag that you should verify with a professional," or "If a request seems to conflict with the user's stated project goals, say so before proceeding." You can read your rules, edit them, version them, and share them with your team.

**Skills** — Documented procedures, best practices, and reference implementations that an agent consults before performing specific types of work. Skills are the difference between a junior employee and a senior one — not raw intelligence, but access to the right playbook and knowing when to apply it. In practice, a skill is a markdown file that lives in the agent's environment: it might contain step-by-step instructions for creating a formatted report, a checklist for code review, best practices for a specific document type, or a reference architecture for a recurring task. Skills can be added, refined, versioned, and shared. You can download a skill someone else developed, drop it into your agent's workspace, and immediately benefit from their accumulated trial and error. A growing ecosystem of published skills already exists.

**Tools** — External capabilities the agent can invoke: web search, code execution, file creation, database queries, API calls, integrations with other services. Tools extend what the agent can *do*. The selection and configuration of tools is a management decision — giving an agent access to the right tools for its role is analogous to giving an employee the right software, access permissions, and resources.

**Workflows** — Structured patterns for how work flows through agent interactions: sequencing, checkpoints, handoffs, tool usage, and output routing. Workflows represent operational architecture. A workflow might specify: research first, then analyze, then synthesize into a recommendation; or: draft, then review against criteria, then revise.

**Context** — The information the agent has access to for a given task. This includes the immediate prompt, but also persistent context like memory of past conversations, reference documents, project background, and knowledge bases. Context is the agent's equivalent of institutional knowledge and situational awareness.

These five mechanisms — rules, skills, tools, workflows, and context — form the **mechanism layer**: the infrastructure through which agent behavior is shaped, developed, and refined over time. Managing agents well means managing this layer well.

What's important to emphasize is that none of these mechanisms are mysterious or require specialized technical knowledge. Rules are sentences you write. Skills are documents you maintain. Tools are integrations you enable or disable. Workflows are sequences you design. Context is knowledge you curate. An information worker who can write a clear email, maintain a team wiki, and design a process checklist already has the core competencies needed to manage the mechanism layer. The gap is not capability — it's recognizing that these familiar management activities now apply to agents, not just people.

#### An Observation

Hughes Johnson spends 480 pages arguing that companies must make implicit structures explicit. Agents require this by default. You cannot manage an agent with unwritten expectations, tribal knowledge, or the assumption that shared context will fill in the gaps. Every behavioral expectation must be encoded in rules. Every relevant procedure must be captured in skills. Every piece of domain knowledge must be surfaced in context. Every workflow must be specified.

Agent management is what happens when you take Hughes Johnson's advice with perfect discipline: everything is documented, everything is version-controlled, and behavioral expectations are codified rather than assumed. The difference is that with agents, the codification is not just good practice — it's the only way the system works at all.

---

### Operating Principles, Translated

Hughes Johnson's four operating principles map to agent management with more fidelity than you might expect — particularly once you account for the mechanism layer.

#### Build Self-Awareness → Build Mutual Capability Awareness

Hughes Johnson's first and most important principle: know your values, your work style, your strengths, and your capability gaps before trying to lead others. She recommends journaling about moments of energy and drain, using assessments like DiSC or MBTI to map your tendencies, and writing a "Working with Me" document that captures how you operate.

**For agents:** Both the manager and the agent need awareness of the agent's capabilities, limitations, and working patterns. This is not only a manager-side exercise. Through rules, the agent itself can carry and apply self-knowledge — "I tend to be verbose on summary tasks," "I am unreliable on precise numerical calculations," "When asked about events after my training cutoff, I should search rather than guess."

The "Working with Me" document maps directly to a well-maintained rules file. The difference: the rules file is executable. It doesn't just inform collaborators; it actively shapes the agent's behavior.

The initial version of this framework asserted that "agents don't introspect." This is too simplistic. While an agent doesn't spontaneously reflect on its own nature, it can — through structured retrospectives — assess its recent performance, identify patterns in what worked and what didn't, and propose updates to its own rules with manager approval. This is not fundamentally different from how human self-awareness develops. Humans don't spontaneously introspect either; they develop self-awareness through deliberate, structured reflection. The mechanism is different (rules files vs. neural pathways), but the management pattern — structured reflection leading to behavioral change — is the same.

#### Say the Thing You Cannot Say → Close the Specification Gap

Hughes Johnson's second principle, inspired by Fred Kofman's *Conscious Business*: surface the unspoken tensions. Don't over-filter. Name the thing everyone is thinking but no one will say.

**For agents, this principle operates in two directions.**

**Manager → Agent:** The biggest failure mode in agent management is under-specification. The "left-hand column" — Kofman's term for what you're thinking but not saying — manifests as the gap between what the worker knows and what they actually put in the prompt. Rules, skills, and persistent context partially solve this: they carry forward information the manager would otherwise need to re-specify every session. The manager's job shifts from "say everything every time" to "build up the rules, skills, and context so I don't have to."

**Agent → Manager:** This is the underappreciated direction. Through rules, an agent can be designed to push back constructively — flagging when a request conflicts with established goals, pointing out ambiguity, challenging assumptions rather than silently complying. Left to defaults, most agents will over-comply, which is the agent equivalent of the organizational silence Hughes Johnson warns against. The manager must deliberately configure the agent to say the hard thing.

*Example: A rule like "If the user's request requires you to make more than two significant assumptions, list them before proceeding and ask for confirmation" turns the agent into an active partner rather than a passive executor.*

#### Distinguish Management from Leadership → Distinguish Orchestration from Direction

Hughes Johnson draws on Marty Linsky: management creates stability through human-centric execution; leadership drives change by setting vision and direction. Both are essential. The balance depends on context — experienced employees need mostly leadership; junior employees need mostly management.

**For agents, three distinct modes map to the mechanism layer:**

| Mode | Human Frame | Agent Frame | Mechanism |
|---|---|---|---|
| **Orchestration** | Running teams, maintaining stability | Configuring workflows, maintaining consistent outputs, monitoring reliability | Workflows, Tools |
| **Direction** | Setting vision, driving change | Defining objectives, choosing what to delegate, deciding when to restructure | Rules |
| **Development** | Training, coaching, skill-building | Adding skills and reference knowledge, refining procedures, expanding tool access | Skills, Context, Tools |

Hughes Johnson references Heifetz's distinction between technical and adaptive problems. This maps cleanly to agents: technical problems (defined solution, clear resolution) are solvable via better skills, context, or workflows. Adaptive problems (continuously evolving, requiring judgment about values and tradeoffs) require rule-level changes — new priorities, new constraints — and often require the manager to make judgment calls that the agent cannot. Knowing which type of problem you're facing before deciding whether to delegate it is a core agent management skill.

#### Come Back to the Operating System → Maintain an Agent Operating System

Hughes Johnson's fourth principle: have a repeatable operating system for every team you manage — clear missions, stated goals, metrics that matter, meeting structures, and cadences. Revisit every six months.

**For agents, the operating system is the full stack of rules, skills, tools, workflows, and context for a given configuration.** It is directly analogous to Hughes Johnson's company OS, with one crucial advantage: it is fully explicit and version-controlled.

| Human OS Component | Agent OS Component | Mechanism |
|---|---|---|
| Mission | Why this agent configuration exists | Rules |
| Goals | Success criteria for current task classes | Rules |
| Metrics | Output quality, reliability, efficiency measures | Workflows |
| Cadence | Retro and review schedule | Workflows |
| Values and principles | Behavioral constraints, tone, pushback triggers | Rules |
| SOPs and playbooks | Documented procedures for specific task types | Skills |
| Institutional knowledge | Domain reference material, past decisions | Context |
| Tool access and permissions | Which integrations and capabilities are enabled | Tools |

**Hygiene:** Periodic audits should cover all five mechanisms. Are rules current, or conflicting, or stale? Are skills up to date, or does the agent still follow deprecated procedures? Is context accurate? Are tools appropriate for current tasks? Are workflows producing good outcomes, or do checkpoints need to move?

---

### The Retro Pattern: The Core Management Loop

Before walking through Hughes Johnson's core frameworks, we need to establish the practice that makes everything else work. In human management, the feedback and coaching apparatus is distributed across informal conversations, 1:1 meetings, formal reviews, and performance improvement plans. For agents, all of these compress into a single repeatable loop: the retrospective.

```
1. TASK      → Agent performs work guided by current rules/skills/tools/workflows/context
2. EVALUATE  → Manager assesses output against success criteria
3. RETRO     → Manager and agent jointly review what worked and what didn't
4. DIAGNOSE  → Attribute the gap to the right mechanism layer
5. UPDATE    → Modify rules, skills, tools, workflows, or context (with manager judgment)
6. VERIFY    → Test the updated configuration against similar tasks
7. PERSIST   → Commit the change; the agent is now better at this class of work
```

The critical step is **diagnosis** — attributing the gap to the correct layer. Hughes Johnson distinguishes between three types of performance fixes for humans: operational/tactical (the environment is wrong), skills fit (the person lacks the ability), and behavioral/attitudinal (the person can do it but doesn't approach it correctly). These map to the mechanism layer:

| Human Performance Fix | Agent Mechanism Layer | Example |
|---|---|---|
| Operational/tactical | **Workflow or tools** | The agent can do the analysis, but the output goes to the wrong place, or it lacks access to the right data source |
| Skills fit | **Skills or context** | The agent doesn't know the right procedure; adding a skill document with step-by-step instructions or domain reference material solves the problem |
| Behavioral/attitudinal | **Rules** | The agent produces correct output but in the wrong tone, at the wrong length, or without flagging uncertainty |
| Wrong person for the job | **Wrong agent** | The model fundamentally can't do this task class; swap, don't refine |

*Example: An agent consistently produces research summaries that are accurate but too academic for the intended audience. The manager's instinct might be to add more context about the audience. But if the agent already has audience context and is ignoring it, the problem is at the rules layer — the agent needs a behavioral guideline like "Write for a busy executive who wants implications and actions, not methodology and caveats." Diagnosing at the wrong layer wastes effort. A different failure — the agent produces summaries that miss key industry context — might be a skills gap, solvable by adding a skill document that outlines how to structure competitive research for this industry.*

What makes the retro pattern powerful is that it compresses the entire human coaching cycle — which might take weeks or months — into something that can execute in minutes, with changes that take effect immediately, results that are directly measurable, and rollback that is free. And because every change is a file edit — a rule updated, a skill document revised, a workflow adjusted — the entire improvement history is visible and reversible.

---

### Foundations and Planning

#### Founding Documents → Agent Configuration as Codified Intent

Hughes Johnson insists that every company needs founding documents: a mission statement, long-term goals, values, and team charters. These guide decision-making from top to bottom. She also recommends team-level charters — one-page documents that articulate why a team exists, what its jobs are, and what others can expect from it.

**For agents, the founding documents are the configuration itself:**

- **Mission** becomes the core purpose statement in the agent's rules: "This configuration exists to help the user draft and refine client-facing communications."
- **Values** become behavioral constraints in rules: what to prioritize when tradeoffs arise, what tone to use, when to push back.
- **SOPs** become skills: documented procedures the agent follows for specific task types, capturing best practices that would otherwise live in someone's head.
- **Team charter** becomes a per-configuration charter: what tasks this agent handles, what it doesn't, what tools it uses, what its known limitations are.

Hughes Johnson references Edgar Schein's three levels of organizational culture: artifacts (observable behaviors), espoused values (stated beliefs), and basic underlying assumptions (deep, often unconscious norms). This framework is illuminating for agents:

1. **Artifacts** → the agent's observable outputs (format, tone, structure)
2. **Espoused values** → your explicit rules, skills, and context documents
3. **Underlying assumptions** → the model's deep training, RLHF, and constitutional principles

The gap between layers 2 and 3 — between what your rules and skills say and what the model's training does — is the source of most agent management frustration. Your rules can override some default behaviors but not all. Understanding which defaults you can and cannot change through the mechanism layer is a core agent management skill, just as understanding the gap between a company's stated values and its actual culture is a core leadership skill.

#### Goals and Metrics → Task Specification and Evaluation

Hughes Johnson uses the mnemonic FOCUS(S) for good goals: Focused, Objectively assessable, Challenging but possible, User-oriented, States not activities, Sensitive and specific. She emphasizes that goals should describe end states, not activities — if a goal starts with a verb like "launch" or "build," it's probably an action, not an outcome.

This transfers directly. An agent task specification that says "research competitors" is an activity. One that says "produce a comparison table of the five largest competitors by revenue, market share, and product focus, with a one-paragraph synthesis of our key differentiators" is a state. The second version is dramatically more likely to produce useful output — and a skill document that captures this specification pattern means you don't have to reinvent it each time.

Hughes Johnson also proposes a critical formula: **Performance = Results × Behaviors.** It's multiplicative. Great results achieved through toxic behavior score zero. For agents, the equivalent is **Output Quality = Accuracy × Alignment × Consistency.** An agent that produces correct output in the wrong format for the wrong audience at unpredictable quality levels is not performing well, even if the facts are right.

- **Accuracy** — is the output correct? (Primarily a model capability issue, assisted by good skills and context)
- **Alignment** — does it follow the specified format, tone, and constraints? (Primarily a rules issue)
- **Consistency** — does it produce similar quality across similar inputs? (Addressed through skills and workflows that reduce variance)

#### Accountability → Trust Tiers

Hughes Johnson describes accountability mechanisms — weekly team meetings, metrics reviews, QBRs — and makes the important distinction that accountability is not the same as monitoring. It's about shared progress, not surveillance.

For agents, the accountability question becomes: *how much review does each type of agent output require?* The answer should be determined before invocation, not after, and it should evolve over time as the mechanism layer matures:

| Tier | Description | Mechanism-Layer Maturity |
|---|---|---|
| **Auto-ship** | Output goes directly to its destination with no human review | Mature rules, proven skills, relevant context, verified workflow; retros have demonstrated reliability |
| **Scan-and-ship** | Quick human pass for obvious errors | Good rules and skills, but edge cases aren't fully covered |
| **Review-and-edit** | Human substantially engages before use | Rules and skills are still being developed through active retros |
| **Collaborate** | Human and agent iterate together | Minimal task-specific configuration; agent contributes capability, human contributes judgment |
| **Human-only** | Agent is not involved | Task requires judgment, relationships, or stakes where agent involvement is inappropriate |

**The key insight is graduation.** Trust tiers should rise over time for a given task class, as rules and skills mature through retros. A task that starts at "collaborate" should, after enough cycles, graduate to "review-and-edit" or "scan-and-ship." Each graduation is backed by evidence — retro logs showing consistent quality. This is the explicit, measurable version of earning trust in human management.

*Example: A PM starts using an agent to draft weekly stakeholder updates. Initially, it's a collaboration — the PM outlines the key points and the agent drafts, then the PM heavily edits. After several cycles and retro-driven updates — new rules ("lead with decisions made, not activities completed"; "keep to 200 words"; "flag blockers in bold") and a skill document capturing the format and tone of successful updates — the task graduates to review-and-edit. After a few more months, it's scan-and-ship: the PM reviews for factual accuracy but rarely changes the structure or tone. The rules file, the skill document, and the retro log are all readable artifacts that document exactly how this graduation happened.*

---

### Hiring → Agent Selection and Configuration

#### Evaluating Agents Across the Mechanism Stack

Hughes Johnson describes a rigorous interview process: structured rubrics, STAR-method questions, work sample tests, Bar Raiser programs, and hiring committees. The goal is to evaluate not just what a candidate knows, but how they work, how they learn, and how they'll fit.

Before deploying an agent on real work, the same rigor applies — evaluated across the full mechanism stack:

| Evaluation Dimension | What You're Testing | Human Hiring Parallel |
|---|---|---|
| **Baseline capability** | Can this model do this task at all, with no special configuration? | Resume screen — basic qualifications |
| **Rule responsiveness** | Does the agent reliably follow behavioral guidelines? Can you shape its behavior? | Interview — does the candidate take direction? |
| **Skill absorption** | Does the agent effectively follow skill documents — applying procedures, checklists, and best practices you provide? | Work sample — can they apply frameworks to real problems? |
| **Tool proficiency** | Does the agent use available tools effectively and appropriately? | Technical screen — can they use the required systems? |
| **Context absorption** | Does it incorporate reference documents and domain knowledge into its work? | Domain expertise — do they understand the subject matter? |
| **Workflow fitness** | Does it work well within structured sequences and handoffs? | Team fit — can they collaborate within existing structures? |
| **Retro capacity** | Can it productively self-assess, identify issues, and propose improvements? | Coachability — do they learn from feedback? |

That last dimension — retro capacity — has no direct parallel in Hughes Johnson but is enormously practical. An agent that can participate productively in retrospectives is far more valuable than one that only executes. It's the difference between an employee who actively seeks feedback and one who waits to be told.

*Example: You're evaluating two models for a research synthesis role. Model A produces slightly better first drafts. Model B produces adequate first drafts but, when asked to retro on its output, accurately identifies its own weaknesses ("I over-indexed on the most recent sources and didn't weigh the longitudinal data enough") and proposes specific rule and skill changes. Model B is the better hire.*

#### Onboarding → Configuration as Cumulative Investment

Hughes Johnson's onboarding framework covers three things: the "why" (mission, story), the "what" (current priorities, goals), and the "how" (behaviors, operating principles). She also recommends sharing the "informal org chart" — not just reporting lines, but key decision-makers, domain experts, incentive structures, and unwritten norms.

For agents, every interaction is potentially a mini-onboarding. But with a mature mechanism layer, onboarding becomes a cumulative investment rather than a per-session cost:

| Phase | Human Version | Agent Version |
|---|---|---|
| **Initial setup** | First 90 days: cover the why, what, how | Build initial rules, author key skills, curate context, configure tools, establish workflows. One-time investment. |
| **Ongoing development** | Career conversations, evolving priorities | Update rules through retros, develop new skills as task classes expand, add context as new domains arise, adjust tools and workflows. The retro loop. |
| **Per-task briefing** | N/A — humans remember | Residual per-session context: what's specific to this task and can't be encoded in persistent rules, skills, or context. With a mature mechanism layer, this becomes small. |

The maturity of the mechanism layer directly determines how much per-task briefing is needed. This is the difference between a well-onboarded employee who needs minimal ramp-up for each new assignment and a contractor who needs extensive briefing every time.

A practical advantage worth emphasizing: when you onboard a new team member in a human organization, you can't hand them a senior colleague's expertise in a file. With agents, you can. A mature set of rules and skills developed through months of retros with one agent can be shared with a colleague, applied to a different model, or used as the starting point for a new configuration. The onboarding investment is portable in a way that human expertise never is.

Hughes Johnson's "informal org chart" maps to an agent ecosystem map: when an agent operates within a system of tools and integrations, its rules and context should encode awareness of the ecosystem — what tools are available, what each is for, when to use what, what data sources exist, where outputs should go. This is the executable version of teaching a new hire how the organization actually works.

---

### Team Development → Ensemble Design and Delegation

#### Team Structures

Hughes Johnson distinguishes between permanent teams (persistent jobs to be done) and working groups (temporary missions). She warns: don't let temporary structures persist too long. If a working group needs to last past a few months, your overall structure is wrong.

This maps directly. Standing agent configurations with persistent rules, skills, and context (your daily writing assistant, your research agent) are permanent teams. Ad hoc agent chains spun up for a specific project are working groups. The same warning applies: ad hoc configurations that become permanent without investment — rule refinement, skill development, retro-driven improvement — will degrade in effectiveness over time.

#### Diagnosing State: The Skill-Reliability Matrix

Hughes Johnson uses Max Landsberg's skill-will matrix: assess each team member along two dimensions — their ability to do the task (skill) and their motivation (will).

For agents, the "will" axis transforms. Agents don't have motivation, but they do have **reliability** — behavioral consistency. Does the agent deploy its capabilities dependably, or does it sometimes fail to apply rules and skills it has access to, produce inconsistent output for similar inputs, or silently degrade on edge cases? Reliability, unlike motivation, is directly improvable through the mechanism layer.

| | High Reliability | Low Reliability |
|---|---|---|
| **High Skill** | Deploy with confidence; graduate trust tier | Diagnose via retro: rule conflicts? Missing or contradictory skills? Stochasticity where determinism is needed? |
| **Low Skill** | Agent reliably flags its own limitations (good self-knowledge rules) → add skills and context, or swap | Don't use this agent for this task |

#### Delegation: The Three-Dimensional Framework

Hughes Johnson uses a framework similar to Jeff Bezos's Type 1/Type 2 decisions: evaluate tasks along two axes — impact (high or low) and reversibility (trapdoor or adjustable). She notes that under-delegation leads to micromanagement and over-delegation leads to losing touch with quality.

For agents, a third axis matters: **mechanism maturity** — how well-developed the rules, skills, tools, workflows, and context are for that task class.

- **Impact**: What's at stake? Who sees the output? What decisions does it feed?
- **Reversibility**: Can the output be corrected, or does it trigger irreversible downstream effects?
- **Mechanism maturity**: How many retro cycles has this task class been through? How mature are the rules and skills?

High mechanism maturity shifts tasks toward greater delegation, even for high-impact work. This is the agent equivalent of Hughes Johnson's insight that you delegate more to experienced, proven team members. And the retro pattern is the mechanism through which maturity increases — each successful cycle justifies expanding scope.

*Example: A first draft of an investor memo is high-impact and somewhat irreversible (once circulated, impressions form). If your agent configuration for memo-writing is new and untested, you collaborate closely and review heavily. After six months of retros — refining rules about tone and structure, developing a skill document that captures the memo format with examples of strong and weak outputs — the same task might be review-and-edit. The impact hasn't changed, but your confidence in the mechanism layer has. And if a colleague needs to produce similar memos, you can share the rules and skill files directly.*

Hughes Johnson also identifies three reasons a manager should personally take on work they could delegate: modeling (showing what "good" looks like), urgency (faster to do it yourself), and resource constraints (not enough people). All three apply to agents, with an important nuance: *modeling is how you develop the skills and rules that eventually allow delegation.* Doing the task yourself first is often the fastest way to build the mechanism layer, because you learn what "good" looks like well enough to specify it — and then you can capture that knowledge in a skill document rather than keeping it in your head.

#### Meetings and Interaction Patterns

Hughes Johnson's PAL framework for meetings — Purpose, Agenda, Limit — transfers directly to agent interactions. Every invocation should have a clear purpose (what am I trying to produce?), an agenda (what specific outputs am I requesting?), and a limit (what scope and length constraints apply?).

Her advice on decision modes is also useful. Be explicit about the mode you're using:

- **Autocratic**: I've decided; execute this.
- **Consultative**: Present options and a recommendation; I'll decide.
- **Delegated**: Decide and execute; I trust your judgment on this.

Most people default to autocratic mode with agents ("write this specific thing") and never use consultative or delegated modes, leaving significant value on the table.

---

### Feedback and Performance

#### Hypothesis-Based Coaching → Hypothesis-Based Retros

Hughes Johnson describes a coaching approach rooted in hypothesis formation: gather data on a report's performance, form a hypothesis about their strengths and development areas, then test the hypothesis — sometimes directly with the person. She notes that if your hypotheses are usually correct after three to six months, your manager's intuition is developing.

This maps directly to retro-driven agent improvement, with the mechanism layer making diagnosis more precise:

| CHJ Coaching Step | Agent Retro Step | Advantage |
|---|---|---|
| Gather data | Collect agent outputs; note successes and failures | Data is recorded, reproducible, and directly comparable |
| Form hypothesis | Attribute the gap to a mechanism layer | Precise: is it rules, skills, tools, workflows, context, or the model itself? |
| Test hypothesis | Update the relevant layer and evaluate | Immediate effect; A/B comparison is trivial; rollback is free |

Hughes Johnson's calibration check applies: if your retro-driven changes usually improve output, your agent management intuition is developing. If they don't, you may be diagnosing at the wrong layer — adding context when the real issue is a missing skill, refining rules when the real issue is the wrong model.

#### Feedback: Direct and Layer-Specific

Hughes Johnson offers a key insight about human feedback: don't offer solutions before you both agree on the problem. With agents, the equivalent is: don't immediately rewrite the prompt. First, diagnose which layer the problem lives in.

| Feedback | Layer | Fix |
|---|---|---|
| "This is too long for the audience" | Rules | Add a behavioral constraint: "For [audience], limit output to [length]" |
| "You missed the regulatory implications" | Context | Add reference material on the regulatory landscape |
| "You formatted this report wrong" | Skills | Add or update a skill document with the correct report format, including examples |
| "You have the right analysis but no recommendation" | Skills or Rules | Add a skill with the expected analysis-to-recommendation structure, or a rule: "Always end analysis with a recommendation and rationale" |
| "You keep citing sources that don't exist" | Rules or Model | Add a rule: "Do not cite specific sources without verification"; or accept this as a model limitation and swap |

A rules fix for a skills problem won't work. A context fix for a rules problem won't either. Getting the layer right is the difference between productive feedback and wasted effort.

#### Formal Reviews → Periodic Configuration Reviews

Hughes Johnson opposes the trend of abolishing formal performance reviews. Her argument: companies that claim to rely on "continuous feedback" still make performance and promotion decisions behind the scenes — and when employees discover this, trust is destroyed. Formal reviews, done well, create transparency about how people are measured and what good looks like.

For agents, the equivalent is periodic configuration reviews — stepping back from task-by-task retros to assess the overall health of a configuration:

```
AGENT CONFIGURATION REVIEW

Configuration: [name]
Review period: [dates]
Task classes: [list]

RULES
- Which rules are producing intended behaviors? (Keep)
- Which are being ignored or overridden by model defaults? (Strengthen or remove)
- Which behavioral patterns need new rules? (Add)
- Are any rules conflicting? (Resolve)

SKILLS
- Are skill documents current and effective?
- Were there errors caused by missing procedures or outdated best practices? (Add or update)
- Are there skill documents the agent never references? (Prune)
- What skill gaps were revealed by recent retros? (Develop)
- Are there skills from other teams or public sources worth adopting? (Import)

TOOLS
- Are the right tools configured? Are any missing? Any unused?
- Is the agent using tools appropriately, or over/under-using them?

CONTEXT
- Is reference material current and relevant?
- Were there errors caused by missing domain knowledge? (Add)
- Is there context the agent never uses? (Prune)

WORKFLOWS
- Is sequencing producing good outcomes?
- Are checkpoints at the right places?
- What changes would improve efficiency or quality?

PERFORMANCE
- Accuracy: [trend]
- Alignment: [trend]
- Consistency: [trend]
- Efficiency: [cost, time, rework rate]
- Trust tier: [current tier; should it change?]

SCOPE DECISION
- Maintain / Expand to [new task classes] / Contract from [task classes] / Retire
```

#### Managing High Performers: Over-Confidence and Over-Compliance

Hughes Johnson identifies two types of high performers: **Pushers** (ambitious, critical, always seeking more responsibility; risk alienating teammates) and **Pullers** (take on any task, deliver reliably; risk burning out silently).

Agents don't have ambition or burnout, but they have failure modes that rhyme:

| Human Type | Agent Failure Mode | Mechanism Fix |
|---|---|---|
| **Pusher** (over-reaches, can alienate) | **Over-confident**: attempts tasks beyond capability; produces plausible but wrong output rather than admitting uncertainty | Rules: add self-knowledge boundaries and uncertainty-flagging ("If confidence is low, say so before proceeding") |
| **Puller** (takes on too much, burns out silently) | **Over-compliant**: says yes to everything; produces mediocre output on tasks it shouldn't have accepted | Rules: add constructive-pushback rules ("If a task is outside your demonstrated strengths, flag this and suggest alternatives") |

Hughes Johnson's advice for high performers — don't assume they're "good enough," challenge them to improve, periodically push them into stretch assignments — transfers directly. Periodically stress-test high-performing configurations against harder tasks. Run retros on the stretch work. This is how you expand scope responsibly.

#### Managing Low Performers: Fix or Deprecate

Hughes Johnson describes a phased approach to low performance: recognize the pattern (Phase 0), align on the problem (Phase 1), agree on next steps (Phase 2), and create a formal improvement plan (Phase 3). She emphasizes forming a hypothesis about the likely outcome before you begin.

For agents, the phases map to the mechanism layer:

| Phase | Action | Mechanism Question |
|---|---|---|
| **0: Pattern recognition** | Errors become recurring | Is this a rules/skills/tools/context/workflow problem, or a fundamental model limitation? |
| **1: Mechanism-layer fixes** | Attempt targeted improvements | Update rules → add or revise skills → add context → adjust tools → modify workflow. Run retros after each change. |
| **2: Evaluate** | Did the fixes work? | If not, you've confirmed the problem is at the model level — no amount of mechanism-layer refinement will solve it. |
| **3: Swap or retire** | Don't limp along | Document what didn't work. A retired configuration's retro log and skill documents are institutional knowledge that prevents repeating mistakes. |

Hughes Johnson's most quotable line on this topic: "Don't let bad hires linger — organizational scars take surprisingly long to heal." Replace "hires" with "configurations" and it's equally true. Bad agent workflows create bad habits, erode trust in AI tools generally, and produce compounding quality problems downstream. The emotional and organizational cost of swapping an agent is far lower than firing a person — which should make the decision easier, though inertia and sunk cost in prompt engineering are real.

---

### The Agent-Augmented Worker

#### Attention Economics

Hughes Johnson's final chapter is about managing yourself — your time, your energy, your resilience. The more senior you become, she writes, "the more creative reality gets at finding ways to beat you up every day."

For the agent-augmented worker, the scarcest resource shifts. The bottleneck is no longer production — agents can produce faster than you can consume. The bottleneck is **attention**: the cognitive bandwidth to evaluate, refine, and direct agent output. Every task you delegate to an agent creates a review obligation, and if you review everything with equal intensity, you've gained nothing.

The mechanism layer is the solution. As rules, skills, tools, workflows, and context mature through retros, the amount of review needed per output decreases. Trust tiers rise. The attention budget is front-loaded — building the mechanism layer is intensive — but then pays compounding dividends as auto-ship and scan-and-ship outputs increase.

The psychological discipline Hughes Johnson describes for human management applies here too: you need the confidence to let auto-ship outputs go without reviewing them, once retros have verified reliability. The temptation to "just check" everything defeats the purpose of delegation.

#### The Core Competency

Hughes Johnson writes that "a leader has to spend their time on things no one else can do." For the agent-augmented information worker, the thing no one else can do is build and maintain the mechanism layer — make the judgment calls that determine rules, develop the skills that encode best practices, curate the context that provides institutional knowledge, select and configure the tools, and design the workflows that orchestrate everything.

This is the new core competency. The worker's comparative advantage in an agentic world is not doing the work (the agent does that) or even directing the work (the rules and skills do that). It is *managing the system* through which agents become increasingly effective over time. It is, in other words, management.

And it is management that is, for the first time, fully accessible to anyone who can write clearly and think systematically about what "good" looks like. The mechanism layer is made of documents, not code.

---

### Conclusion and Next Steps

The frameworks Hughes Johnson developed for scaling human organizations — at Google, at Stripe, now at Harvard Business School — apply to agent management with more precision than casual analogy would suggest. The match is not metaphorical. Goal-setting, delegation, onboarding, structured feedback, performance evaluation, calibration, and scope management are the same disciplines, operating through a different mechanism layer.

The irony is worth restating: agents require by default the codification that Hughes Johnson spent an entire book convincing human organizations to adopt. The information worker who manages agents well will be the one who makes the implicit explicit, builds repeatable systems, runs structured retrospectives, diagnoses at the right layer, and invests in the mechanism infrastructure that compounds over time.

#### What This Framework Needs Next

**Practical templates.** The CHJ-to-agent template mapping in the appendix identifies a dozen templates to develop — from agent readiness checklists to configuration review templates to delegation checklists. Building and testing these against real workflows is the next concrete step.

**Worked examples and tutorials.** Each section would benefit from walkthroughs showing real agent management scenarios — writing a rules file, developing a skill document, running a retro that produces a specific mechanism-layer change. The retro pattern in particular needs concrete demonstrations at each layer.

**Research integration.** This framework is built on one source text and first-principles reasoning. It should be stress-tested against emerging literature on agentic workflows, human-AI teaming, and organizational design for AI-augmented work. Specific areas to research: existing agentic frameworks (LangChain, CrewAI, AutoGen) and how they map to the mechanism layer; organizational trust models for AI systems; the emerging practice of prompt engineering as a management discipline.

**The team-level question.** This document focuses on the individual information worker managing their own agents. But organizations will face a collective version of the same challenge: who manages the shared mechanism layer when a team uses agents? Is this a new role? How do you calibrate agent performance across a department? Hughes Johnson's frameworks for organizational design and cross-team coordination become relevant at this level. The portability of skills and rules — the fact that a team can share, standardize, and version-control its agent configurations — makes this tractable in ways that human management knowledge-sharing never was.

---

### Epilogue: Where the Analogy Breaks

No analogy is perfect, and claiming otherwise would undermine the framework's credibility. Several aspects of human management don't transfer to agents, or transfer in inverted form. These are documented here for completeness and because some of them point to genuinely new territory.

**Motivation.** Agents don't have intrinsic motivation. The "will" axis of the skill-will matrix doesn't fully collapse — it transforms into reliability/consistency — but the management interventions are different. You can't inspire an agent; you can reduce its variance.

**Emotional intelligence and psychological safety.** Not applicable to agents directly. But deeply relevant to how humans feel about working alongside agents — and to how teams adopt agent workflows. The manager's emotional intelligence is still critical; it's just directed at the human side of the human-agent system.

**Career development.** Agents don't have careers. But their configurations do mature: they accumulate rules, skills, context, and workflow refinements; they earn expanded scope through demonstrated reliability. This is closer to human professional development than it first appears, but it lacks the intentionality and self-direction that makes human career growth meaningful.

**Firing.** You deprecate, swap, or constrain agent configurations. The emotional and organizational cost is much lower than firing a person, which changes the calculus entirely — you should be much faster to swap a failing agent than to fire a struggling employee. But sunk cost in prompt engineering and workflow inertia are real friction.

**Stochasticity.** Humans vary in performance due to mood, energy, context, and growth. Agents vary due to sampling and temperature. Same input can produce different output. This is a fundamentally different kind of variance that requires different management responses — primarily at the workflow layer (adding verification steps) or the rules layer (adding self-consistency checks).

**Duplication, composability, and cost.** You can run the same agent on 50 tasks simultaneously. You can chain agents into pipelines. Every action has a measurable, immediate cost. These have no human parallel and represent genuinely new management territory that this framework does not yet fully address.

**Version control and transferability.** You can snapshot an agent's entire behavioral configuration, diff changes, and roll back. You can port a mature mechanism layer to a new model or share it across a team. Human expertise is not transferable in this way. This is arguably the single most important structural advantage of agent management over human management, and it deserves deeper exploration.

---

### Appendix: Templates to Develop

| CHJ Template | Agent Management Analogue | Primary Mechanism |
|---|---|---|
| Working with Me doc | Agent rules file (capabilities, limitations, style, preferences) | Rules |
| SOPs / playbooks | Skill documents (procedures, checklists, best practices, reference implementations) | Skills |
| Management Prerequisites Checklist | Agent Readiness Checklist (before deploying on a task class) | All |
| OKR template | Agent Task Specification (objective, success criteria, constraints) | Rules, Skills |
| QBR outline | Agent Configuration Review (periodic full-stack audit) | All |
| Interview Framework & Rubric | Agent Evaluation Rubric (baseline, rule responsiveness, skill absorption, tool proficiency, context absorption, workflow fitness, retro capacity) | All |
| Performance Review template | Agent Configuration Review by mechanism layer | All |
| PIP template | Mechanism-layer Improvement Plan (targeted changes, evaluation criteria, timeline) | Targeted |
| Team Charter | Agent Config Charter (purpose, scope, tools, skills, limitations) | Rules, Skills |
| Delegation conversation steps | Agent Task Delegation Checklist (purpose, context, deliverable, constraints, trust tier) | Workflows |
| Offsite planning doc | Agent Ecosystem Review (full mechanism-layer audit) | All |
| Calibration process | Cross-configuration comparison (for teams using multiple agents) | All |

### Appendix: Key Concepts Index

1. **The Mechanism Layer** — rules, skills, tools, workflows, and context as the infrastructure through which agent behavior is shaped
2. **The Retro Pattern** — the core management loop: task → evaluate → retro → diagnose → update → verify → persist
3. **Mediated Introspection** — agents can develop functional self-awareness through rules, updated via retros
4. **Constructive Pushback Rules** — rules designed to make the agent surface concerns, flag ambiguity, and challenge assumptions
5. **Trust Tiers with Graduation** — auto-ship / scan-and-ship / review-and-edit / collaborate / human-only; tiers rise with mechanism maturity
6. **Layer-Specific Diagnosis** — attributing performance gaps to rules, skills, tools, workflows, context, or the model itself
7. **The Delegation Cube** — impact × reversibility × mechanism maturity
8. **Attention Economics** — the bottleneck shifts from production to evaluation; mechanism maturity reduces review overhead
9. **Agent OS** — the full mechanism stack for a configuration, analogous to CHJ's company operating system
10. **The Skill-Reliability Matrix** — adapted from skill-will, with reliability (behavioral consistency) as the manageable axis
11. **Output Quality = Accuracy × Alignment × Consistency** — the agent equivalent of Performance = Results × Behaviors
12. **The Espoused-vs-Underlying Gap** — distance between explicit rules/skills and deep model behavior, per Schein's culture layers
13. **The Forced-Explicit Irony** — agents require by default the codification CHJ spends 480 pages advocating
14. **Retro Capacity** — an agent evaluation dimension: can the agent productively self-assess and propose improvements?
15. **Mechanism-Layer Portability** — mature rules and skills can be shared, imported, and applied across agents, teams, and models
