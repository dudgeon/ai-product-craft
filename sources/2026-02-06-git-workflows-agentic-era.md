---
created: 2026-02-06
updated: 2026-02-07
template: templates/source.md
template_version: 2
tags: [source, ai-pm-craft, organic]
status: read
source_type: article
source_url: ""
archive_url: "domains/professional-development/ai-pm-craft/sources/2026-02-06-git-workflows-agentic-era.md"
author: "Dudgeon (organic)"
published: 2026-02-06
discovered: 2026-02-06
summary: "Two git patterns for agentic workflows: (1) subtree push to publish private repo folders to public repos with history intact, (2) submodules to import external repos as agent context. CLAUDE.md bridges both contexts. Prediction: team knowledge repos become first-class infra; submodules get reputation upgrade because agents handle the ceremony humans find annoying."
domain: professional-development
project: ai-pm-craft
---

# Git Workflows for the Agentic Era: Sharing Context Across Repository Boundaries

**By**: Dudgeon (organic/self-authored)
**Source**: Self-authored blog post
**Type**: article (organic)

## Summary

Repository boundaries are shifting from code isolation to context boundaries. Git subtree (publish outward) and submodules (import inward) solve the mechanics; CLAUDE.md files bridge the gap by documenting relationships for agents. The key reframe: submodules' ceremony is only painful for humans — agents handle it trivially, and explicit version pinning becomes a feature for reproducibility. Team knowledge repos (markdown, not wikis) are emerging as first-class infrastructure.

## Key Ideas Extracted

*Fill during processing. Each idea links to a knowledge entry.*

## Notes

*Your annotations, reactions, questions, disagreements. Written during or after reading.*

## Raw Content

As more development work happens inside agentic tools like Claude Code and Windsurf, the relationship between repositories is changing. Your agent needs access to everything relevant to do its job well—but "everything relevant" increasingly spans multiple repos with different ownership and visibility.

This post covers two patterns I've been refining:

1. **Publishing outward**: Exposing select folders from a private repo to public repos, automatically
2. **Importing inward**: Pulling external repos into your workspace so your agent has full context

Both patterns optimize for the same thing: letting you work in one place while your agent sees the full picture.

---

## The Setup: A Private Knowledge Repo

I maintain a private repo called `home-brain`—a personal knowledge base, project archive, and workspace. It contains things I want to keep private, but also material I want to share:

- `claude/` — my Claude Code configuration, instructions, and skills
- `ai-pm-craft/` — notes on how AI is changing product management

I want to publish both of these to separate public repos (`home-brain-config` and `ai-pm-craft`) so others can see and use them. But I don't want to context-switch between repos while working. I want to edit everything in `home-brain` and have the public repos stay in sync automatically.

---

## Pattern 1: Publishing Folders to Public Repos

### Why Not Just Copy Files?

You could write a GitHub Action that copies files from your private repo to a public one. But you lose git history, and the public repo becomes a dead mirror rather than a proper git project.

**Git subtree** solves this cleanly. It extracts a folder with its commit history intact and pushes it to another repo. The public repo gets real commits, not just file dumps.

### Manual Subtree Push

If you want explicit control over when things go public:

```bash
# Push claude/ folder to home-brain-config repo
git subtree push --prefix=claude git@github.com:youruser/home-brain-config.git main

# Push ai-pm-craft/ folder to ai-pm-craft repo
git subtree push --prefix=ai-pm-craft git@github.com:youruser/ai-pm-craft.git main
```

Your workflow: edit in `home-brain`, commit and push normally, then run the subtree push when you're ready to publish.

### Automatic Sync with GitHub Actions

For a fully hands-off approach, add a workflow that syncs on every push:

```yaml
# .github/workflows/sync-public-repos.yml
name: Sync folders to public repos

on:
  push:
    branches: [main]
    paths:
      - 'claude/**'
      - 'ai-pm-craft/**'

jobs:
  sync-claude:
    if: contains(github.event.head_commit.modified, 'claude/') || contains(github.event.head_commit.added, 'claude/')
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
        with:
          fetch-depth: 0
      - name: Push to home-brain-config
        run: |
          git config user.name "github-actions"
          git config user.email "actions@github.com"
          git subtree push --prefix=claude https://x-access-token:${{ secrets.PUBLIC_REPO_TOKEN }}@github.com/youruser/home-brain-config.git main

  sync-ai-pm-craft:
    if: contains(github.event.head_commit.modified, 'ai-pm-craft/') || contains(github.event.head_commit.added, 'ai-pm-craft/')
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
        with:
          fetch-depth: 0
      - name: Push to ai-pm-craft
        run: |
          git config user.name "github-actions"
          git config user.email "actions@github.com"
          git subtree push --prefix=ai-pm-craft https://x-access-token:${{ secrets.PUBLIC_REPO_TOKEN }}@github.com/youruser/ai-pm-craft.git main
```

To set this up:

1. Create a GitHub Personal Access Token with `repo` scope
2. Add it as a repository secret called `PUBLIC_REPO_TOKEN` in your private repo
3. Create the public repos (can be empty)
4. Commit the workflow file

Now every push to `main` that touches `claude/` or `ai-pm-craft/` automatically syncs to the public repos.

### CLAUDE.md in Published Folders

Here's a nice side effect: Claude Code supports `CLAUDE.md` files at any directory level. A `claude/CLAUDE.md` in your private repo gets picked up when working in that directory. When subtree pushes it to the public repo, it becomes the root `CLAUDE.md` there.

The same file serves both contexts—directory-level instructions in your private repo, root instructions in the public one.

---

## Pattern 2: Importing External Repos for Agent Context

Now the inverse scenario. Your team maintains a shared knowledge repo—style guides, API documentation, architectural decisions, prompt libraries. You're working in your own project repo, but you want your agent to have access to all that context.

This is what **git submodules** are actually good for.

### Adding a Submodule

```bash
# In your project repo
git submodule add https://github.com/your-org/team-knowledge.git external/team-knowledge
git commit -m "Add team-knowledge as submodule"
```

Now `external/team-knowledge/` contains the full contents of that repo. Your agent can read, search, and reference anything in it.

### Where the Config Lives

Two places, both committed to your repo:

**`.gitmodules`** at your repo root:
```ini
[submodule "external/team-knowledge"]
    path = external/team-knowledge
    url = https://github.com/your-org/team-knowledge.git
```

**A commit pointer** in git's tree—the submodule directory is tracked as a SHA, not files. This pins it to a specific version until you explicitly update.

### The Traditional Pain Points

Submodules have a bad reputation because:

- Cloning doesn't fetch submodule contents by default
- You need `git clone --recursive` or `git submodule update --init`
- Staying current requires manual update commands
- Forgetting to commit the pointer after updating causes confusion

### The Agentic Workaround

Here's the reframe: if your collaborators are working through agents, the agent can handle the ceremony. Add this to your `CLAUDE.md`:

```markdown
## External Context (Submodules)

This repo includes submodules in `external/` containing reference material from shared team repos.

**At the start of each session:**

1. Ensure submodules are populated:
   git submodule update --init --recursive

2. Check for upstream updates:
   git submodule update --remote

3. If there are changes, commit the updated pointer:
   git add external/
   git commit -m "Update external submodules to latest"

**Why this matters:** The submodules contain team standards, API docs, and shared context that inform how work should be done in this repo. Always ensure you have the latest before starting substantive work.
```

The agent reads this, runs the commands, and the submodule friction disappears. You're writing documentation for an agent audience—and agents don't find submodules annoying.

### Multiple Context Sources

You can import several repos this way:

```bash
git submodule add https://github.com/your-org/api-specs.git external/api-specs
git submodule add https://github.com/your-org/style-guide.git external/style-guide
git submodule add https://github.com/your-org/prompt-library.git external/prompt-library
```

Your agent now has access to API contracts, coding standards, and vetted prompts—all discoverable in the file tree, all searchable, all part of its working context.

---

## The Emerging Pattern

What I'm describing is a shift in how we think about repository boundaries. The old model: repos are isolated, you clone what you need, you manage dependencies through package managers and build systems.

The new model: your agent needs rich, contextual access to multiple sources of truth. Some you own, some you don't. Some are public, some private. The boundaries matter for access control and attribution, but your working context should be unified.

Git's existing tools—subtree and submodules—handle the mechanics. What's new is using `CLAUDE.md` and similar agent instructions to document the relationships and automate the maintenance.

A few predictions:

**Team knowledge repos will become first-class infrastructure.** Not wikis or Notion pages, but git repos full of markdown that agents can read. Style guides, architectural decisions, prompt libraries, workflow documentation.

**Submodules will get a reputation upgrade.** Their ceremony is only annoying for humans. Agents handle it fine, and the explicit version pinning becomes a feature—you can see exactly what context the agent had when it made a change.

**"Import this repo for context" will become a common onboarding step.** New team member? Clone the project, but also pull in the team knowledge base. Your agent is now calibrated to how we do things here.

---

## Quick Reference

### Publishing a folder to a public repo (one-time)

```bash
git subtree push --prefix=folder-name git@github.com:user/public-repo.git main
```

### Importing an external repo for context

```bash
git submodule add https://github.com/org/repo.git external/repo-name
git commit -m "Add repo-name as submodule"
```

### CLAUDE.md snippet for submodule maintenance

```markdown
## External Context

This repo uses submodules in `external/`. At session start:

1. `git submodule update --init --recursive`
2. `git submodule update --remote`
3. Commit any updates: `git add external/ && git commit -m "Update submodules"`
```

---

The tools aren't new. What's new is the context: agents that can read documentation and act on it, workflows that assume an AI collaborator, and repositories that serve as context sources rather than just code containers.

We're still early in figuring out what good looks like here. But the direction is clear: unified context, automated maintenance, and documentation that speaks to both human and agent readers.
