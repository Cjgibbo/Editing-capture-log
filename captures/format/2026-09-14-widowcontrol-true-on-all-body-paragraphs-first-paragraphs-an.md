---
date: 2026-09-14
category: format
tier: 3
destination: system-prompt
summary: "widowControl: true on all body paragraphs, first paragraphs, and block quotes prevents single stranded lines."
---

# widowControl: true on all body paragraphs, first paragraphs, and block quotes prevents single stranded lines.

**Tier:** 3
**Destination:** system-prompt

## Detail

Applied to: makeBodyParagraph, makeFirstParagraph, makeBlockQuote, and inline no-indent paragraphs built after section headings. Prevents fewer than 2 lines at the top or bottom of a page break. This is a hard rule for all templates. LibreOffice honors this property when converting docx to PDF.
