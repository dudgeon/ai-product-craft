---
created: 2026-02-21
updated: 2026-02-21
tags: [meta, spec, feature, ai-pm]
status: draft
---

# Copy as Markdown — Feature Spec

## Goal

Let readers copy any page's content as clean Markdown so they can paste it directly into an LLM chat window. The site already renders well-structured knowledge entries and source notes — this feature makes that content portable with one click.

## Approach: Runtime HTML-to-Markdown Scraping

Uses [Turndown.js](https://github.com/mixmark-io/turndown) (standard open-source HTML-to-Markdown converter) to scrape the rendered page content at runtime. No persisted Markdown files, no build pipeline changes, no GitHub API calls.

**How it works:**
1. Button click lazy-loads Turndown.js + GFM plugin from cdnjs (~14KB, loaded only on first use)
2. Clones `.main-content`, strips non-content elements (copy button, heading anchors, edit links)
3. Converts the cleaned HTML to Markdown via Turndown
4. Prepends the source URL so the reader (and their LLM) knows where it came from
5. Copies to clipboard via native Clipboard API

**What gets copied:**
```
Source: https://ai-pm.cc/knowledge-base/product-lifecycle/build/context-first-development/

# Context-First Development

## Summary

The single most common failure mode in AI-assisted development...
```

## Button Placement & UX

- **Position**: Top-right of the `.main-content` area, above the page title
- **Label**: Clipboard icon + "Copy as Markdown"
- **After click**: Checkmark icon + "Copied!" for 2 seconds, then resets
- **Failure**: Falls back to copying visible text with source URL prepended

## Nested Copy Button Prevention

**Not an issue in practice.** Each Jekyll page is a separate HTML document — pages don't embed other pages' rendered content in the DOM. The JavaScript:

1. Runs once on `DOMContentLoaded`
2. Checks for an existing `.copy-page-btn` before injecting (guard clause)
3. Injects exactly one button per page

Index/listing pages link to child pages but don't inline their content.

## Technical Implementation

### Single file changed

| File | What |
|------|------|
| `_includes/head_custom.html` | Inline `<style>` + copy button JS below existing TOC script |

Everything is self-contained in this one include: CSS, button injection, Turndown lazy-loading, clipboard logic. No changes to `_sass/`, `_layouts/`, `_config.yml`, or the sync workflow.

**Deployment**: Copy the updated `head_custom.html` to the `dudgeon/ai-pm` public repo's `_includes/` directory. The sync workflow is not involved (it excludes `_includes/` by design).

### Dependencies

- **Turndown.js** (7.2.0) — loaded from cdnjs CDN on first click, not bundled
- **turndown-plugin-gfm** (1.0.2) — adds table support, also from cdnjs CDN
- No npm packages, no build steps, no vendored files

### Content cleaning before conversion

Elements stripped from the clone before Turndown processes it:

| Selector | Why |
|----------|-----|
| `.copy-page-wrapper` | The copy button itself |
| `a.anchor-heading` | Just-the-docs heading anchor SVGs (would convert to junk markdown) |
| `.edit-this-page` | "View source on GitHub" link |

## Edge Cases

| Case | Handling |
|------|----------|
| Turndown CDN unreachable | Falls back to `innerText` copy with source URL |
| Browser doesn't support Clipboard API | Button click is a no-op; extremely rare in 2026 |
| Page is an index/listing page | Works the same — scrapes and converts that page's content |
| User has JS disabled | Button doesn't appear (injected via JS) — no broken UI |
| Tables on the page | Handled by turndown-plugin-gfm; degrades gracefully without it |
