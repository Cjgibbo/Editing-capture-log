---
date: 2026-09-14
category: format
tier: 3
destination: system-prompt
summary: "keepNext: true on all section headings and sub-headings prevents orphan headers at page bottom."
---

# keepNext: true on all section headings and sub-headings prevents orphan headers at page bottom.

**Tier:** 3
**Destination:** system-prompt

## Detail

Without keepNext, section headings (Montserrat SemiBold 13pt) and sub-headings (Crimson Pro Bold Italic 11pt) could render as the last element on a page with no body text following — the heading orphans at the bottom. Adding keepNext: true and keepLines: true to both paragraph types forces at least one body paragraph to follow the heading onto the same page. If there isn't room, the heading moves to the next page. This is a hard rule for all templates.
