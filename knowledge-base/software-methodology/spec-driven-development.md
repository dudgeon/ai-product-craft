---
created: 2026-02-14
updated: 2026-02-14
template: templates/knowledge-entry.md
template_version: 5
tags: [knowledge, ai-pm, mental-model, software-methodology, spec-driven, ai-coding]
status: draft
entry_type: mental-model
origin: sourced
featured: false
domain: software-methodology
project: ai-pm
---

# Spec-Driven Development

## Summary

Software can ship as specs and tests with zero implementation code — AI agents handle the implementation in any target language. Drew Breunig's `whenwords` library demonstrates the pattern: a SPEC.md defining behavior, a tests.yaml with language-agnostic test cases, and a one-line prompt for agents to implement, test, and place the code. No dependency management, no version lock-in, always a fresh implementation.

The model works for simple, stable, "implement-and-forget" utilities — well-bounded functions against well-defined standards where performance isn't critical and the spec won't change. It breaks down fast for anything requiring iterative debugging (probabilistic code can't be replicated between builds), cross-language test matrices at scale (testing surface grows exponentially), security patching (updates need to reach all users), community support (no shared codebase to rally around), or performance optimization (hand-tuned code still wins for critical paths).

The real mental model for PMs: classify your product components along a spectrum from "utilities" (spec-drivable, implement-and-forget) to "foundations" (requiring traditional development investment, community, and ongoing maintenance). The boundary between these categories shifts as models improve — but community, support infrastructure, and iterative debugging don't go away just because implementation gets cheaper.

## How to Apply

**When to use**: When evaluating which parts of a software product could adopt AI-native delivery patterns. When arguing for or against spec-driven approaches in architectural decisions. When a stakeholder asks "if coding is free, why do we need engineers?"

**When not to use**: Don't apply this as a binary — it's a spectrum, not a toggle. Most real products contain both utility-like components (good candidates) and foundation-like components (poor candidates). Don't use it to argue that all code should become specs, or that specs can never replace code.

**Classification criteria for spec-drivable components**:
- Simple utilities vs. complex frameworks → utilities can be spec-driven
- Well-defined standards (like time formatting, unit conversion) → good candidates
- Not performance bottlenecks → implementation differences don't matter
- Stable and unchanging → no need for security patches or iterative updates
- Language-agnostic value → benefit from cross-language implementation

**Why foundations still need code**:
1. **Performance**: Browsers, databases, rendering engines need hand-optimized code
2. **Testing complexity**: Cross-language × cross-agent test matrices grow exponentially (SQLite: 51,445 tests vs. whenwords: 125)
3. **Debugging**: Can't replicate bugs in probabilistically generated code — each rebuild is different
4. **Updates**: Security patches and bug fixes must reach all users deterministically
5. **Community**: Bug discovery, contributor velocity, interoperability, and cultural practices require shared implementations

**For AI PMs**: This mental model helps you answer the strategic question "what do engineers do when coding is free?" — they build the foundations, maintain the community, and make judgment calls about which components belong on which side of the spectrum.

## Sources

### From: [2026-02-06 Spec Driven Development No Code Library](../../sources/2026-02-06-spec-driven-development-no-code-library.md)
**Key quote**: "Community isn't just about the code — it's about the ongoing maintenance, support, testing, and cultural practices around software. Spec-only libraries work for 'implement and forget' utilities but fail when you need the ecosystem that makes software dependable and evolvable."
**Attribution**: Drew Breunig
**What this source adds**: The foundational case study — `whenwords` as a concrete implementation of spec-only delivery, with a thorough analysis of where the pattern breaks. The five failure modes (performance, testing, debugging, updates, community) form the framework for evaluating spec-drivability.
**Links**: [Original](https://www.dbreunig.com/2026/01/08/a-software-library-with-no-code.html) | [Archive](../../sources/2026-02-06-spec-driven-development-no-code-library.md)

## Related

- [Context First Development](../product-lifecycle/build/context-first-development.md) — The biggest mistake in AI-assisted dev is rushing past context; spec-driven development is the extreme case of context-first: the entire deliverable is context (specs + tests)
- [Interactive PRD Writing](../product-lifecycle/build/interactive-prd-writing.md) — PRD-as-input-to-AI parallels spec-as-input-to-AI; both represent the shift from writing implementation to writing specification
