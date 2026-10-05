---
date: 2026-09-15
category: parser
tier: 3
destination: build-log
summary: "Heading hierarchy detection must be per-chapter, not global — chapters without "Part N:" structure should promote all headings to section_head."
---

# Heading hierarchy detection must be per-chapter, not global — chapters without "Part N:" structure should promote all headings to section_head.

**Tier:** 3
**Destination:** build-log

## Detail

First pass before parsing body: const hasPartStructure = lines.some(l => /^Part\s+\d+\s*:\s*.+$/.test(cleanText(l)));

If chapter has Part structure: "Part N:" lines → section_head (Montserrat SemiBold 14pt), all other title-case headings → sub_head (Crimson Pro Bold Italic 11pt).

If chapter has NO Part structure (e.g., Ch 1): all detected headings → section_head.

A single global heuristic that assigns everything without "Part" to sub_head makes Ch 1's headings ("Speed Beyond Imagination," "The G-Force Reality") render at the wrong visual weight.
