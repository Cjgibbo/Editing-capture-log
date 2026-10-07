---
date: 2026-10-07
category: format
tier: 3
destination: build-log | style-reference
summary: "Brent (Alexander Printing) reviewed Tier 3 .docx output and provided seven formatting corrections"
---

Brent's handwritten review of the pre-export .docx (Rain Master / Stride template):

1. TOC too large — compress to one line per chapter
2. Widow word on p. 8 → pull back to p. 7
3. Excessive space between subheadings
4. Question mark on Ch. 1 title — verify intentional
5. Graphic on p. 12 should fit on p. 11
6. Remove small caps after subheadings
7. Too many paragraph breaks — AI parser is splitting too aggressively at context shifts; needs a wider threshold for what triggers a new paragraph

Item 7 is the most consequential for the pipeline. Brent's framing: if the AI marks a paragraph break every time context changes, the gap needs to be wider to produce natural-length paragraphs. This affects both the current prompt-based pipeline and the future standalone app's parser logic.

Items 1, 3, and 6 are template-level changes (TOC styling, subheading spacing, post-subheading small caps). Items 2 and 5 are per-book pagination adjustments. Item 4 is a content verification flag.
