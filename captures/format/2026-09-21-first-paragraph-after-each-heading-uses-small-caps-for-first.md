---
date: 2026-09-21
category: format
tier: 3
destination: style-reference
summary: "First paragraph after each heading uses small caps for first four words — no indent."
---

# First paragraph after each heading uses small caps for first four words — no indent.

**Tier:** 3
**Destination:** style-reference

## Detail

Implementation: smallCaps: true on a TextRun containing the first four words, followed by normally-formatted TextRuns for the rest of the paragraph. No firstLine indent on this paragraph. Verified rendering: LibreOffice preview shows "IMAGINE THIS: YOU'RE STRAPPED" in small caps style (all-caps rendering in fallback font, but Word will show proper small caps with Crimson Pro installed). Every section heading and sub-heading resets the "first paragraph" flag.
