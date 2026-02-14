---
created: 2026-02-05
updated: 2026-02-14
tags: [project, ai-pm, product-management, learning]
status: active
domain: professional-development
pattern: domain-source-synthesis
source_types: [article, video, podcast, book-chapter, organic, note]
---

# AI PM <span class="site-subtitle">{craft, tools, mental models, ideas...}</span>

A knowledge base for AI-augmented product management — how PMs use AI tools effectively and how product organizations adapt to AI-native ways of working. Every idea is traceable back to its sources with quotes, context, and links.

## Structure

```
ai-pm/
├── sources/           Source material with full attribution and reading status
├── knowledge-base/    Extracted knowledge organized by domain
│   ├── product-lifecycle/               Mapped to six lifecycle phases (vertical)
│   │   ├── discover/                    What problems are worth solving?
│   │   ├── frame/                       What does success look like?
│   │   ├── shape/                       What solution takes form?
│   │   ├── build/                       How do we ship with clarity?
│   │   ├── release/                     How do we put this into the world?
│   │   └── measure/                     Did it work, and what's next?
│   ├── horizontal/                      Lifecycle-agnostic AI PM skills (stack by delivery mechanism)
│   │   ├── prompting/                   Portable techniques (any chat window)
│   │   ├── context/                     Knowledge infrastructure (discoverability, KM)
│   │   ├── runtimes/                    Templated AI runtimes (GPTs, Gems, Claude Projects)
│   │   └── agents/                      Building & managing knowledge agents
│   ├── ai-adoption/                     Org change and adoption
│   └── software-methodology/            How AI changes software delivery paradigms
└── meta/              Project ontology, taxonomy, and lifecycle framework
```

## Sources

Source material is the raw input — articles, podcasts, newsletters, and organic experience. Each source gets a structured note with attribution, key quotes, and extracted ideas.

**Pipeline**: `unread` → `reading` → `read` → `processed`

Browse all sources and their status in the [Source Registry](sources/), or jump to [unread sources](sources/#unread).

## Knowledge Base

Knowledge entries are ideas extracted from sources and organized by domain. Entries improve over time as more sources corroborate them.

**Entry types**: `technique` · `mental-model` · `insight`
**Entry status**: `draft` → `solid` (multiple sources) → `canonical` (vetted, teachable)

Browse all entries in the [Knowledge Map](knowledge-base/README.md).

## Taxonomy & Meta

Classification rules, lifecycle framework, and entry templates live in `meta/`. See [taxonomy.md](meta/taxonomy.md) for how entries are categorized.

---

## Status

Early stage. 31 sources captured, 8 fully processed into 25 knowledge entries. 19 unread sources in the queue. Entries span Build, Shape, Context, Prompting, Agents, and AI Adoption. Templated AI Runtimes and Software Methodology Evolution domains awaiting source processing to populate.

---

## Related

- Context: `context/professional.md`
