---
date: 2026-09-21
category: format
tier: 3
destination: build-log
summary: "Copyright page bottom alignment requires split spacer paragraphs — single large spaceBefore is capped by LibreOffice."
---

# Copyright page bottom alignment requires split spacer paragraphs — single large spaceBefore is capped by LibreOffice.

**Tier:** 3
**Destination:** build-log

## Detail

A single spacing: { before: 7200 } (5 inches) on the first paragraph is capped by LibreOffice to roughly 0.5" — copyright text stays at top of page. Splitting into three spacer paragraphs at { before: 2160 } each (1.5" × 3 = 4.5") pushes content to lower half of page. The VerticalAlign.BOTTOM section property in the docx library is either not emitted into the XML or not honored by LibreOffice — spacer paragraphs are the reliable workaround.
