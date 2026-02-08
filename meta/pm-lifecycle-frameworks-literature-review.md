---
created: 2026-02-08
updated: 2026-02-08
tags: [meta, ai-pm-craft, literature-review, frameworks]
status: active
domain: professional-development
project: ai-pm-craft
---

# Product Lifecycle Frameworks: A Comprehensive Map of Modern PM Models

**No single product management lifecycle framework dominates the industry, but a clear structural pattern emerges across 12+ major models: virtually all separate problem-understanding from solution-building, yet most fail to treat business case development and success metrics as a first-class lifecycle phase.** This gap matters because teams that bury KPI definition inside "discovery" or defer it to "learn" often ship products without clear success criteria. The proposed six-phase Identify→Define→Design→Deliver→Launch→Learn structure maps cleanly onto the strongest elements of existing frameworks and fills a genuine gap identified in both academic research and practitioner literature. Below is a detailed analysis of every major framework, how AI is reshaping each stage, and where the bodies are buried.

---

## The established frameworks and their phase structures

Twelve widely-adopted frameworks define the modern PM landscape. They fall into three structural archetypes: **parallel-track models** (continuous discovery alongside delivery), **sequential-stage models** (gated progression from idea to launch), and **iterative-loop models** (rapid cycles of build-test-learn). Understanding the archetype matters because it determines where business case development, metrics definition, and learning naturally fit—or don't.

### Parallel-track and continuous models

**Marty Cagan's Dual-Track Agile** splits all product work into two concurrent tracks. The **Discovery Track** (run by the "product trio" of PM, designer, and tech lead) validates ideas against four risks—value, usability, feasibility, and viability—through customer interviews, rapid prototyping, and experiments. The **Delivery Track** builds, tests, and deploys production software through CI/CD. Discovery runs 1–2 sprints ahead of delivery, and both tracks operate continuously in parallel, not sequentially. The key insight: validated backlog items flow from discovery into delivery, while usage data from delivery feeds back into discovery.

**SVPG's Product Operating Model** (formalized in Cagan's 2024 book *Transformed*) extends dual-track into three dimensions: **Product Strategy** (deciding which problems to solve, driven by vision and quarterly focus), **Product Discovery** (solving those problems through prototyping and risk validation), and **Product Delivery** (building, deploying, and measuring). The model rests on empowered product teams assigned problems rather than feature roadmaps. Twenty principles span five concepts: culture, strategy, teams, discovery, and delivery. This is SVPG's most comprehensive articulation to date.

**Teresa Torres' Continuous Discovery Habits** structures ongoing discovery around the **Opportunity Solution Tree (OST)**. Teams start with a desired product outcome, conduct **weekly customer interviews** (the "keystone habit"), map unmet needs into a hierarchical opportunity tree, generate multiple solutions per opportunity, and then test underlying assumptions rather than whole ideas. The framework defines 11 specific habits and six mindsets (outcome-oriented, customer-centric, collaborative, visual, experimental, continuous). It does not prescribe sequential phases—it's a parallel cadence designed to run continuously alongside delivery.

### Sequential-stage models

**The Double Diamond** (Design Council, 2005, updated 2019) divides work into two diamonds of divergent-then-convergent thinking. The first diamond covers **Discover** (ethnographic research, stakeholder interviews, market analysis) and **Define** (affinity diagramming, persona development, problem framing). The second diamond covers **Develop** (brainstorming, prototyping, co-design) and **Deliver** (usability testing, design handoff, staged rollout). Adopted by IDEO, Google, Microsoft, and hundreds of design programs. Its weakness: **no explicit business case, metrics, or post-launch learning phase**.

**Stage-Gate** (Robert Cooper, 1980s) is the most structured model, with **six stages separated by five gates** (go/kill decisions). Stage 0: Discovery/Ideation → Stage 1: Scoping → **Stage 2: Build the Business Case** → Stage 3: Development → Stage 4: Testing & Validation → Stage 5: Launch. Each gate requires senior leaders to assess quality of execution, business motivation, and strategic alignment. **Stage 2 is the gold standard for business case as a distinct phase**—it demands market research, financial modeling (NPV, ROI), voice-of-customer data, and a complete action plan. The fifth-generation "NexGen" Stage-Gate integrates agile sprints within stages.

**Pragmatic Institute's Framework** maps **37 activity boxes across 7 categories**: Market (market problems, competitive landscape), Focus (market definition, product roadmap), Business (business plan, pricing, profitability), Planning (personas, requirements, use scenarios), Programs (marketing plan, launch, awareness), Enablement (sales alignment, channel training), and Support (operations, measurement). This is the most comprehensive lifecycle-oriented framework in PM and explicitly includes both a **Business Case** activity and a **Performance and Analytics** activity as discrete responsibilities.

**AIPMM's ProdBOK** (Product Management Body of Knowledge) defines **7 lifecycle activities**: Conceive → Plan → Develop → Qualify → Launch → Deliver → Retire. Modeled after PMI's PMBOK, it's the most formally structured lifecycle in PM and uniquely includes end-of-life management as an explicit phase.

### Iterative-loop models

**Lean Startup's Build-Measure-Learn** (Eric Ries) is a tight feedback loop: build an MVP, measure with actionable metrics, learn whether to persevere or pivot. Ries recommends planning in reverse—decide what to learn first, then what to measure, then what to build. The broader lifecycle progresses from problem-solution fit → product-market fit → scale. **By design, it has no upfront business case**—it substitutes experimentation for planning.

**Melissa Perri's Product Kata** (from *Escaping the Build Trap*) adapts Toyota Kata into four steps: understand the direction → analyze the current condition → set the next target condition → experiment via PDCA cycles. Within this, she defines three phases of product work: **problem exploration, solution exploration, and solution optimization**. Her strategy deployment framework layers Company Vision → Strategic Intent → Product Initiatives → Options. A key principle: a feature isn't "done" when it ships—it's done when it achieves the desired outcome.

**Shape Up** (Basecamp/Ryan Singer) operates in fixed **six-week cycles** with three phases: **Shaping** (senior staff define the problem, set appetite, sketch a solution, and identify risks), **Betting** (the "Betting Table" selects projects—no backlog), and **Building** (teams discover scopes, build end-to-end, track via Hill Charts). A **circuit breaker** kills projects that don't ship within six weeks. The two-week cooldown between cycles handles bugs and tech debt.

### Strategy and evaluation frameworks

**Reforge's Product Strategy Stack** defines five hierarchical layers: Company Mission → Company Strategy → Product Strategy → Product Roadmap → Product Goals. All product work falls into four categories: **Feature Work** (strengthening current PMF), **Growth Work** (optimizing acquisition/retention/monetization loops), **PMF Expansion** (entering new segments), and **Scaling Work** (infrastructure, process, user scaling). Reforge's Ravi Mehta Competency Model maps 12 PM competencies across Product Execution, Customer Insight, Product Strategy, and Influencing People.

**Gibson Biddle's DHM Model** evaluates product strategy through three lenses: **Delight** (does it create customer value?), **Hard-to-copy** (does it build durable competitive advantage via network effects, brand, scale?), and **Margin-enhancing** (does it generate profit to reinvest?). His broader toolkit includes the GLEe Model (Get big → Lead → Expand) and GEM Model (Growth, Engagement, Monetization prioritization).

---

## How AI is reshaping each lifecycle stage

A 2025 Springer systematic review of 190 publications found that **no widely adopted, systematic framework for AI-driven product management across all lifecycle phases currently exists**. However, several practitioner frameworks and emerging models are filling this gap rapidly.

### The most complete AI-PM frameworks

**Curtis Savage's U.S.I.D.O. Framework** is the most structured AI-PM lifecycle model published to date. Its five phases—**Understand** (AI analyzes product analytics and unstructured data like app reviews to spot patterns), **Strategize** (LLMs generate SWOT and competitive analysis from company context), **Ideate** (AI generates feature recommendations tied to specific goals), **Define** (AI prioritizes features, writes PRDs, predicts feature impact on KPIs), and **Optimize** (AI refines GTM strategy, identifies key metrics, runs experiment analysis)—map AI capabilities to specific PM activities at each stage. Savage built a custom "AI Product Manager in a Box" GPT to demonstrate the workflow.

**Lenny Rachitsky's Three-Job Model** maps AI disruption across PM work with a counterintuitive finding. He rates PM tasks on a 🤖 scale of 1–5 for AI impact: **Shape the Product** (strategy, discovery, goals—🤖🤖🤖🤖, highest disruption), **Ship the Product** (specs, project management—moderate), and **Sync the Team** (communication, stakeholder alignment—lowest disruption). His contrarian insight: **high-level strategic skills will be most disrupted by AI, while soft skills become more valuable**. Andrew Ng's observation, shared by Lenny, that PM is becoming the "new bottleneck"—with teams proposing 2:1 PM-to-engineer ratios—underscores this shift.

**Marily Nika's AI-Native Workflow** (Google AI Product Lead) demonstrates end-to-end PM work in under 20 minutes through "tool hopping": user research via **Perplexity** (mining Reddit for raw opinions) → PRD writing via **custom GPT** → prototyping via **Google AI Studio/v0.dev** → stakeholder vision via **Flow/Sora** (video mockups) → evaluation via **NotebookLM**. Her key innovation: **skip the PRD first—go straight from idea to prototype, show engineers, then write the PRD**. This inverts the traditional lifecycle.

The **Product-Led Alliance's seven-phase model** maps AI tools to: Ideation & Conception (ChatGPT/Gemini for brainstorming, Midjourney for visual mockups) → Market Research & Validation (AI sentiment analysis, simulated user interactions) → MVP Design & Prototyping (Visily, Uizard, Galileo AI for wireframing) → Development (AI code generation) → Launch & GTM (AI messaging and targeting) → Post-Launch Analytics (behavioral analytics, anomaly detection) → Iteration & Optimization (continuous AI-driven improvement).

### Key practitioners shaping AI-PM practice

**Reid Robinson** (Lead AI PM at Zapier) focuses on MCP (Model Context Protocols) for PM workflows—connecting Claude with 8,000+ apps to automate CRM updates, meeting prep, and customer feedback synthesis. His philosophy: "Instead of focusing on what's coming in AI, tie it back to the problems we have." **Claire Vo** (CPO at LaunchDarkly) built ChatPRD—an AI copilot used by 10,000+ PMs—over a weekend and hosts the "How I AI" podcast on Lenny's network. She demonstrates going from idea to shipped product in 30 minutes using ChatPRD → Devin for async coding. **Tal Raviv** distinguishes between AI copilots (chat-based) and AI agents (autonomous actors) and argues agents work best for "least favorite, least impactful, but still necessary" PM tasks. His Lenny's Newsletter guest post on AI agents was among the publication's most popular pieces ever.

---

## Mapping frameworks to the six-phase Identify→Define→Design→Deliver→Launch→Learn structure

**The proposed six-phase structure does not exist as a published framework**—searches for this exact sequence returned zero results. However, it synthesizes elements from multiple established models in a way that addresses recognized gaps. Here is how each major framework maps:

| Framework | Identify | Define | Design | Deliver | Launch | Learn |
|-----------|----------|--------|--------|---------|--------|-------|
| **Double Diamond** | Discover | Define | Develop | Deliver | — | — |
| **Stage-Gate** | Discovery + Scoping | Business Case ✓ | — | Development + Testing | Launch | — |
| **SVPG Product Model** | Discovery (problem) | Strategy | Discovery (solution) | Delivery | Delivery (rollout) | Delivery (measure) |
| **Dual-Track Agile** | Discovery Track | Discovery Track | Discovery Track | Delivery Track | Delivery Track | Both tracks |
| **Torres CDH** | Interviewing + Opportunity mapping | Outcomes definition | Solution ideation | — | — | Assumption testing |
| **Perri Product Kata** | Understand direction + Current condition | Target condition | — | Experiment | — | Learn from experiments |
| **Lean Startup** | — | — | Build (MVP) | Build | — | Measure + Learn |
| **Shape Up** | Shaping (problem) | Shaping (appetite) | Shaping (solution sketch) | Building | — | — |
| **Pragmatic Institute** | Market + Focus | Business ✓ | Planning | — | Programs | Support + Measurement |
| **AIPMM ProdBOK** | Conceive | Plan | — | Develop + Qualify | Launch + Deliver | — (Retire) |
| **Pendo PMLC** | Discover | Phase 0: Business Outcome ✓ | Validate | Build | Launch | Iterate |
| **U.S.I.D.O.** | Understand | Strategize | Ideate | Define | — | Optimize |

The frameworks that **most cleanly map** to the six-phase structure are **Stage-Gate** (which has the closest phase alignment including an explicit business case), **Pragmatic Institute** (which covers all six phases across its activity categories), and **Pendo's PMLC** (six phases with an explicit business outcome definition). The Double Diamond maps well to the first four phases but lacks Launch and Learn entirely. Continuous models like Torres and Cagan resist mapping to sequential phases because they're designed as parallel cadences.

---

## How PM communities organize knowledge—and what it reveals

A striking pattern emerges in how PM knowledge is taxonomized. **Formal certification bodies organize by lifecycle stage, while practitioner communities organize by skill domain.** AIPMM's ProdBOK follows Conceive→Plan→Develop→Qualify→Launch→Deliver→Retire. Pragmatic Institute structures 37 activities across 7 lifecycle categories. But Reforge organizes courses by competency (Product Foundations, Mastering Analytics, Growth Strategy). Lenny's Newsletter taxonomizes by problem type (product-market fit, pricing, career growth). Mind the Product uses topic categories (Product Strategy, Product Growth, Stakeholder Management). ProductPlan uses a hybrid—their product navigation implicitly follows Discovery→Strategy→Prioritization→Roadmaps→Launch, while educational content is skill-based.

The **Ravi Mehta/Reforge PM Competency Model** has become particularly influential, organizing 12 competencies into four quadrants: Product Execution (specs, delivery, quality), Customer Insight (data fluency, voice of customer, UX), Product Strategy (business outcomes, vision, strategic impact), and Influencing People (stakeholders, leadership, managing up). This model explicitly shifts emphasis as PMs become more senior: from execution → strategy → people influence.

The implication for a lifecycle-based knowledge taxonomy: it must account for the fact that **modern PM education has moved away from "what to do at each stage" toward "what skills to develop."** A lifecycle taxonomy succeeds when it bridges both—organizing activities chronologically while mapping skill requirements to each phase.

---

## The business case and metrics gap is real and recognized

The most significant structural gap across PM frameworks is the treatment of **business case development, success metrics definition, and KPI/objective function specification**. This gap manifests in three ways.

First, **development-centric frameworks ignore business justification entirely**. Agile/Scrum has no business case mechanism—it assumes the backlog is already prioritized. The Double Diamond and Design Thinking are user-centric to a fault, with business viability absent from their phase structures. Lean Startup is anti-business-case by design, substituting experimentation for upfront planning.

Second, **metrics frameworks are disconnected from lifecycle timing**. Google's HEART framework (Happiness, Engagement, Adoption, Retention, Task Success), AARRR Pirate Metrics, and the North Star Metric framework all specify *what* to measure but not *when in the lifecycle to define those metrics*. OKR cycles (typically quarterly) often misalign with discovery timelines—as one practitioner noted, "When you define your OKR at the beginning of the quarter, then embark on a six-week discovery phase, you have hardly enough time left to make an impact."

Third, **only three frameworks treat business case as a first-class concern**: Stage-Gate (Stage 2 is literally "Build the Business Case"), Pragmatic Institute (explicit Business Case and Performance Analytics activity boxes), and Amazon's Working Backwards (the internal FAQ section of the PR/FAQ covers financial projections, costs, and success metrics). Pendo's PMLC comes close with "Phase 0: Define Business Outcome" but labels it a precursor rather than a peer phase. Cagan's Opportunity Assessment includes "How will we measure success?" as question #8, but buries it within discovery.

Pragmatic Institute published one of the few resources that explicitly links *which* metrics matter *when*—their "23 Metrics Mapped to Product Life Cycle" maps specific metrics to Development, Launch, Growth, Maturity, and Decline phases. This kind of lifecycle-aware metrics mapping is exactly what most frameworks lack.

---

## Conclusion: where the six-phase model fits and what it uniquely solves

The proposed Identify→Define→Design→Deliver→Launch→Learn structure occupies a genuine white space in PM frameworks. Its **Define phase—housing stakeholder alignment, business case, and roadmapping between problem discovery and solution design—addresses the most significant structural gap** in modern PM methodology. Stage-Gate proves this works but carries waterfall baggage; the six-phase model can preserve this rigor while operating iteratively.

Three design choices would make this framework distinctive. First, **making business case and success metrics a mandatory gate between Identify and Design** prevents the common failure mode where teams prototype solutions before establishing measurable success criteria. Second, **the Learn phase must feed back into Identify** (not just into the next sprint) to create the strategic learning loop that Melissa Perri's Product Kata and Reforge's strategy framework both emphasize. Third, **AI augmentation maps naturally to this structure**: AI excels at pattern recognition in Identify (user research synthesis), financial modeling in Define (business case generation), rapid prototyping in Design (tools like v0.dev and Galileo AI), spec writing in Deliver (ChatPRD), launch automation in Launch (GTM targeting), and anomaly detection in Learn (behavioral analytics). The framework's six phases create natural "AI insertion points" that the more abstract continuous models lack.

The academic consensus (Witkowski & Wodecki, 2025) confirms: real competitive advantage comes from integrating AI across all lifecycle phases, not just applying it to individual tasks. A lifecycle framework that explicitly defines those phases gives organizations a concrete structure for systematic AI adoption—something no widely-adopted framework currently provides.
