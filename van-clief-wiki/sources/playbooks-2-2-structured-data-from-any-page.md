---
type: source
created: 2026-04-23
updated: 2026-04-23
sources: 1
tags: [playbooks, browser, scraping, module-2]
---

# playbooks-2-2-structured-data-from-any-page

> Source: Implementation Playbooks course, Module 2 Lesson 2.2. Written lesson (video pending). File: `.wiki/raw/playbooks/lesson-2-2-structured-data-from-any-page.md`.

## Summary

Use the Claude for Chrome extension to pull tables, product info, contact details, and other structured data out of any webpage. The lesson walks through a five-step loop: open the sidebar, navigate to the page, describe what you want, receive the result, then ask for the format you need. It covers pagination, scroll-to-load, detail pages, multi-tab comparisons, and a practice target (`books.toscrape.com`). Output formats available: list, table, CSV, bulleted, numbered, JSON. Example prompt patterns are supplied for product research, contact scraping, job listings, review aggregation, and price monitoring.

## Key claims

1. Claude reads what is visible on the page: text, prices, ratings, descriptions, links, tables, lists, and legible image text.
2. Claude does not read: content behind login walls (until you log in manually first), content that only appears after interaction, PDFs, or downloaded files.
3. Pagination, scroll-to-load, and detail-page expansion are handled by direct prompt ("go through the first 5 pages"; "scroll to load all items"; "click into each listing and pull the details").
4. Multi-tab comparison works by dragging tabs into Claude's tab group, then prompting across the group.
5. Frequently-repeated extractions can be saved as sidebar shortcuts, triggered by typing `/` in the sidebar. Recording is covered in Lesson 2.3.
6. Output format is negotiable on request: table, CSV, bulleted, numbered, JSON, plain list.
7. Prompting lessons inherited from Foundation 1.3 apply: be specific, point Claude to a region ("in the main product grid"), start small, ask Claude to verify counts.
8. "Claude pulled the wrong information" is nearly always a specificity failure, solvable by a tighter prompt.
9. The same prompting framework from Foundation 1.3 (Identity, Task, Context, Constraints, Output Format) is the mechanism behind every successful extraction.

## Entities mentioned

- [[van-clief]]
- [[claude-in-chrome]]

## Open questions

- The shortcut-saving UI is described at a high level; exact button labels may drift.
- Rate-limit behaviour across many pages not covered.
