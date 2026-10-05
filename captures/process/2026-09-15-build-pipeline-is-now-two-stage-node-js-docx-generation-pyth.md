---
date: 2026-09-15
category: process
tier: 3
destination: build-log
summary: "Build pipeline is now two-stage: Node.js DOCX generation → Python post-processing → LibreOffice PDF export."
---

# Build pipeline is now two-stage: Node.js DOCX generation → Python post-processing → LibreOffice PDF export.

**Tier:** 3
**Destination:** build-log

## Detail

Stage 1: node build-book.js — parses chapter .docx files via pandoc, assembles full book DOCX with the docx npm library (fonts embedded, images embedded, all formatting).

Stage 2: python3 add-page-numbers.py — opens the DOCX with python-docx, injects footer PAGE fields into chapter and foreword sections, sets first-page suppression.

Stage 3: libreoffice --headless --convert-to pdf — converts to final PDF.

This pipeline exists because the npm docx library doesn't generate footer XML. The standalone app should either fix the npm library usage or build entirely in Python.
