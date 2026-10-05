---
date: 2026-09-21
category: decision
tier: 3
destination: system-prompt
summary: "Tier 3 output format changed from PDF to .docx — reduces token cost, simplifies pipeline, adds editability at the cost of a 30-second manual export step."
---

# Tier 3 output format changed from PDF to .docx — reduces token cost, simplifies pipeline, adds editability at the cost of a 30-second manual export step.

**Tier:** 3
**Destination:** system-prompt

## Detail

All Tier 3 output is now a fully formatted .docx at final trim size. Chris opens in Word, verifies, exports to PDF, sends to Alexander. Style template specs are format-agnostic and needed no changes. Known tradeoffs: orphan/widow control is set as a paragraph property but enforcement depends on the rendering engine; drop caps require XML manipulation in python-docx and may need manual touch; bleed handling for full-bleed image books falls outside the automated pipeline. Token savings are significant — eliminates the reportlab typesetting layer entirely.
