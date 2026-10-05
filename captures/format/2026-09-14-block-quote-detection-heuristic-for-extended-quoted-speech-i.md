---
date: 2026-09-14
category: format
tier: 3
destination: build-log
summary: "Block quote detection heuristic for extended quoted speech in body text."
---

# Block quote detection heuristic for extended quoted speech in body text.

**Tier:** 3
**Destination:** build-log

## Detail

Senna quotes ("I was in a tunnel..." etc.) are not marked as blockquotes in the source — they're regular paragraphs that start and end with quotation marks. Detection heuristic: paragraph starts with " and ends with " and is longer than 120 characters. These render as EB Garamond (now Crimson Pro) Italic 10pt/13pt, left indent 0.5", right indent 0.25", 6pt space above/below. Shorter quoted sentences embedded in narrative paragraphs stay as body text. The 120-char threshold was empirically set from this manuscript — may need adjustment for other manuscripts.
