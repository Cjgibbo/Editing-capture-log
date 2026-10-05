---
date: 2026-09-14
category: format
tier: 3
destination: build-log
summary: "Image insertion sizing uses pixel dimensions scaled to 297×468 max (4.125"×6.5" at 72ppi)."
---

# Image insertion sizing uses pixel dimensions scaled to 297×468 max (4.125"×6.5" at 72ppi).

**Tier:** 3
**Destination:** build-log

## Detail

docx-js ImageRun.transformation takes pixel values (width/height in points). Available area for diagram images: page width minus gutter minus outside margin = 4.125", page height minus top/bottom margins minus caption space ≈ 6.5". Images are scaled proportionally to fit within 297×468 pixels. identify -format "%w %h" gets source dimensions. The SVG diagram (G-force) required conversion to PNG first via rsvg-convert -w 1200. JPG images embed directly.
