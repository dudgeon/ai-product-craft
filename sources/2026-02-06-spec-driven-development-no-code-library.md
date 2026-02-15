---
title: "A Software Library with No Code"
created: 2026-02-06
updated: 2026-02-14
template: templates/source.md
template_version: 2
tags: [source, ai-pm, spec-driven-development, ai-coding]
status: processed
source_type: article
source_url: "https://www.dbreunig.com/2026/01/08/a-software-library-with-no-code.html"
archive_url: "domains/professional-development/ai-pm/sources/2026-02-06-spec-driven-development-no-code-library.md"
author: "Drew Breunig"
published: 2026-01-08
discovered: 2026-02-06
summary: "whenwords library ships specs + tests with zero code — AI agents implement in any language from SPEC.md and tests.yaml. Works for simple, well-bounded utilities; breaks down for complex frameworks needing perf optimization, community support, iterative debugging, and security patches. PM question: which product components are 'implement and forget' utilities vs foundations requiring traditional dev investment?"
domain: professional-development
project: ai-pm
---

# A Software Library with No Code

**By**: Drew Breunig
**Source**: [dbreunig.com](https://www.dbreunig.com/2026/01/08/a-software-library-with-no-code.html)
**Type**: article

## Summary

Breunig's `whenwords` is a thought experiment: what if libraries shipped only specs and tests, with AI handling implementation? It works for small, stable utilities but breaks down fast — debugging probabilistic code, cross-language test matrices, security patching, and community support all require concrete implementations. The real PM takeaway is the classification question: which parts of your product are "implement and forget" utilities vs. foundations that need traditional investment?

## Key Ideas Extracted

- [Spec-Driven Development](../knowledge-base/adjacent-disciplines/spec-driven-development.md) — When specs + tests can replace code; the utility-vs-foundation classification spectrum

## Notes

*Your annotations, reactions, questions, disagreements. Written during or after reading.*

## Raw Content

Drew Breunig released `whenwords`, a relative time formatting library that contains *no code*—only specs and tests. The library can be implemented in any language (Ruby, Python, Rust, Elixir, Swift, PHP, Bash, even Excel) by feeding its SPEC.md and tests.yaml files to an AI coding agent like Claude. This thought experiment explores what software engineering looks like when AI can implement tightly specified code perfectly.

### Key Concept: Spec-Only Libraries

The `whenwords` library consists of three components:
- **SPEC.md**: Detailed behavior and implementation specification
- **tests.yaml**: Language-agnostic test cases (input/output pairs)
- **INSTALL.md**: Simple prompt for AI agents to implement the library

Installation is a single prompt:
```
Implement the whenwords library in [LANGUAGE].

1. Read SPEC.md for complete behavior specification
2. Parse tests.yaml and generate a test file
3. Implement all five functions: timeago, duration, parse_duration,
   human_date, date_range
4. Run tests until all pass
5. Place implementation in [LOCATION]
```

### When Spec-Only Libraries Work

Good candidates for spec-only approaches:
- Simple utilities (vs. complex frameworks)
- Well-defined standards (like Unix time)
- Functions that aren't performance bottlenecks
- Implement-and-forget utilities
- Projects where language-agnostic implementation is valuable

### When Traditional Code Libraries Are Still Necessary

**1. When Performance Matters**
- Complex applications like browsers need hand-optimized code
- Memory management and rendering optimization require human expertise
- Large user base finding and fixing edge cases in production

**2. When Testing is Complicated**
- Updates to specs might work for one language but break others
- Testing surface area grows exponentially (4 AI agents × 20 languages)
- SQLite has 51,445 tests vs. whenwords' 125 tests
- CI/CD complexity becomes unmanageable

**3. When You Need Support & Bug Fixes**
- Replicating bugs is nearly impossible with probabilistic AI generation
- Customer-generated codebases are all different
- Can't iteratively debug a specific implementation
- Each rebuild may produce significantly different code

**4. When Updates Matter**
- Security patches and bug fixes need to reach all users
- Examples: LiteLLM (frequent model additions), nginx, Rails, Postgres
- Spec-only works best for stable, unchanging utilities

**5. When Community & Interoperability Matter**
- Large communities spot more bugs
- More contributors mean faster fixes
- Comprehensive testing enables rapid PR acceptance
- Community support keeps code current
- Culture and collaboration around shared goals
- Reference implementations tie specs to reality

### Implications for AI-First Product Management

**The "Coding is Free" Question**: Recent advancements (Opus 4.5 + Claude Code) crossed a threshold in Q4—models can implement tightly specified code reliably. This raises fundamental questions about software architecture.

**When to Use Spec-Driven Development**:
For simple, well-bounded utilities:
- Pros: Language agnostic, no dependency management, always fresh implementation
- Cons: Inconsistent builds, harder debugging, no community support

For foundations and frameworks:
- Traditional code libraries still essential
- Community, testing, performance, and support outweigh spec-only benefits

**Product Strategy Considerations**:
1. Utility Functions: Could be delivered as specs/tests for AI implementation
2. Core Infrastructure: Needs traditional code with community
3. Enterprise Software: Might ship as "Claude Skills" or prepared contexts
4. Support Model: How do we debug probabilistically-generated customer code?

### Open Questions

- As models improve, does the balance shift?
- Will spec-only libraries develop their own communities around spec maintenance?
- What's the right boundary between spec-driven and traditional development?
- How do we handle versioning and dependency management for specs?
- What testing strategies work at scale for multi-language, multi-agent builds?

### Personal Notes

Key insight: **Community isn't just about the code—it's about the ongoing maintenance, support, testing, and cultural practices around software.** Spec-only libraries work for "implement and forget" utilities but fail when you need the ecosystem that makes software dependable and evolvable.

For PM craft: Think about which parts of your product are "utilities" that could be spec-driven vs. "foundations" that need traditional development investment and community building.
