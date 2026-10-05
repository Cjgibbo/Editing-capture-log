---
date: 2026-09-14
category: format
tier: 3
destination: build-log
summary: "Full book assembly section structure: front matter sections use SectionType.ODD_PAGE for recto starts except copyright page which uses EVEN_PAGE; chapters use ODD_PAGE with titlePage: true for suppressed page numbers on openers."
---

# Full book assembly section structure: front matter sections use SectionType.ODD_PAGE for recto starts except copyright page which uses EVEN_PAGE; chapters use ODD_PAGE with titlePage: true for suppressed page numbers on openers.

**Tier:** 3
**Destination:** build-log

## Detail

Section order: title page (ODD_PAGE, no page numbers) → copyright page (EVEN_PAGE, no page numbers, bottom-anchored) → dedication (ODD_PAGE, no page numbers) → TOC (ODD_PAGE, no page numbers) → foreword (ODD_PAGE, no page numbers) → chapters 1–11 (each ODD_PAGE, arabic page numbers starting at 1 on chapter 1, titlePage: true suppresses footer on chapter openers). Front matter sections use frontMatterFooters() (empty). Chapter sections use chapterFooters() (centered bottom Crimson Pro 10pt page number on default pages, empty on first/title page).
