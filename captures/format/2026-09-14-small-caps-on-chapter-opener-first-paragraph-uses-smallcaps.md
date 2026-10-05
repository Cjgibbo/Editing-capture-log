---
date: 2026-09-14
category: format
tier: 3
destination: build-log
summary: "Small caps on chapter opener first paragraph uses smallCaps: true property, not a separate SC font."
---

# Small caps on chapter opener first paragraph uses smallCaps: true property, not a separate SC font.

**Tier:** 3
**Destination:** build-log

## Detail

The EB Garamond apt package includes a separate EB Garamond SC 12 font file for small caps. When switching to Crimson Pro (no separate SC variant), the implementation changed to smallCaps: true on the TextRun. This is more portable across fonts and should be the standard approach for all templates. The first 4 words of the opening paragraph get the small caps treatment; remaining text continues as normal body.
