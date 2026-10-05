---
date: 2026-09-12
category: format
tier: 2
destination: build-log
summary: "Paragraph indentation convention — first paragraph after a heading gets no indent; subsequent paragraphs get 0.5" first-line indent."
---

# Paragraph indentation convention — first paragraph after a heading gets no indent; subsequent paragraphs get 0.5" first-line indent.

**Tier:** 2
**Destination:** build-log

## Detail

Standard book typesetting: the first paragraph after a chapter title, part heading, or section heading has no first-line indent. All subsequent paragraphs in that section get a 0.5" (720 DXA) first-line indent. This was implemented via a noIndent boolean parameter on the paragraph helper function. Consistent across all five chapters. This matches Chicago Manual of Style convention and standard trade book formatting.
