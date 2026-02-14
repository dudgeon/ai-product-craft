---
created: 2026-02-14
updated: 2026-02-14
template: templates/knowledge-entry.md
template_version: 5
tags: [knowledge, ai-pm, mental-model, context, git, repositories, agent-context]
status: draft
entry_type: mental-model
origin: organic
featured: false
domain: horizontal
horizontal_domain: context
project: ai-pm
---

# Repositories as Context Boundaries

## Summary

In agentic workflows, repository boundaries are shifting from code isolation units to context boundaries. Your agent needs access to everything relevant — but "everything relevant" increasingly spans multiple repos with different ownership and visibility. Git's existing tools handle the mechanics: subtree publishes folders outward (with history intact), submodules import external repos inward (with version pinning). CLAUDE.md files bridge both contexts by documenting relationships for agents.

The key reframe: submodules' notorious ceremony — recursive cloning, manual updates, pointer commits — is only painful for humans. Agents handle it trivially by reading CLAUDE.md instructions and running the commands. The explicit version pinning that frustrated human developers becomes a feature for agents: you can see exactly what context the agent had when it made a change. This transforms a historically reviled git feature into a legitimate context distribution mechanism.

The broader prediction: team knowledge repos (markdown in git, not wikis or Notion) will become first-class organizational infrastructure. "Import this repo for context" becomes a standard onboarding step — clone the project, pull in the team knowledge base, and the agent is calibrated to how we do things here.

## Origin

**Context**: Managing the home-brain system, which publishes select folders (`.claude/`, `ai-pm/`) from a private repo to public repos. The need to work in one unified context while maintaining separate publication boundaries drove exploration of git subtree and submodule patterns.

**How you use it**: Git subtree push syncs private repo folders to public repos with commit history. A GitHub Action automates this on push to main. CLAUDE.md files serve double duty — directory-level instructions in the private repo become root instructions in the published repo. For importing external context, submodules in an `external/` directory make shared team repos available to the agent, with CLAUDE.md documenting the update ceremony.

**Why it works**: Agents read documentation and act on it. The submodule ceremony that frustrated human developers is just a series of git commands that an agent executes without complaint. By writing documentation for an agent audience, pain points that killed adoption for humans simply disappear. The filesystem remains the universal interface — agents don't need special APIs or plugins to access submodule content.

## Related

- [Filesystem as Retrieval Architecture](filesystem-as-retrieval-architecture.md) — Single-repo filesystem as retrieval system; this entry extends the pattern across repository boundaries
- [Filesystem as Agent State](../agents/filesystem-as-agent-state.md) — Filesystem as agent state within one repo; cross-repo context expands the state namespace
- [Deliberate Context Selection](deliberate-context-selection.md) — Hand-picking context files; submodule import is a systematic version of this at the repo level
- [Three-Layer Context Disclosure](three-layer-context-disclosure.md) — READMEs as index layer within repos; CLAUDE.md bridges serve a similar role across repo boundaries
- *Software Methodology Evolution angle*: This pattern also signals how development infrastructure evolves under AI — repos become context containers, not just code containers, and historically painful git features get rehabilitated when agents absorb the ceremony
