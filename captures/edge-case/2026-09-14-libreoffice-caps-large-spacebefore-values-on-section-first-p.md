---
date: 2026-09-14
category: edge-case
tier: 3
destination: build-log
summary: "LibreOffice caps large spaceBefore values on section-first paragraphs; must split into multiple spacer paragraphs."
---

# LibreOffice caps large spaceBefore values on section-first paragraphs; must split into multiple spacer paragraphs.

**Tier:** 3
**Destination:** build-log

## Detail

A single empty paragraph with spaceBefore: 6660 (4.625") at the start of a new docx section renders at approximately 4.0" regardless of the specified value. LibreOffice appears to cap or collapse the space. Fix: split the vertical drop into multiple consecutive empty paragraphs, each with max 1.5" (2160 DXA) of spaceBefore. This produces the correct cumulative drop. Verified: with split spacers, per-chapter overrides of 4.5", 5.25", and 5.5" all render at their specified values.
