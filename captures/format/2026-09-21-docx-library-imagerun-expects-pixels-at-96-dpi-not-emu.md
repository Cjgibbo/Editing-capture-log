---
date: 2026-09-21
category: format
tier: 3
destination: build-log
summary: "docx library ImageRun expects pixels at 96 DPI — not EMU."
---

# docx library ImageRun expects pixels at 96 DPI — not EMU.

**Tier:** 3
**Destination:** build-log

## Detail

The npm docx library's ImageRun transformation: { width, height } takes values in pixels at 96 DPI. It internally multiplies by 9525 to convert to EMU. Passing raw EMU values (e.g., 2,447,925 for 2.68 inches) produces images 9525× too large — extent values in the billions in the XML.

Correct conversion: widthPx = targetWidthInches * 96; heightPx = targetHeightInches * 96.

Verified by inspecting the <wp:extent> and <a:ext> values in the generated XML: 257px * 9525 = 2,447,925 EMU = 2.68". Correct.
