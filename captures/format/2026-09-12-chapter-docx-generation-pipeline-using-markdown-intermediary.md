---
date: 2026-09-12
category: format
tier: 2
destination: build-log
summary: "Chapter .docx generation pipeline using markdown intermediary and docx-js build script."
---

# Chapter .docx generation pipeline using markdown intermediary and docx-js build script.

**Tier:** 2
**Destination:** build-log

## Detail

Workflow: write revised chapter content as .md file → run through a reusable Node.js build script (build-chapter.js) that parses markdown and generates formatted .docx with docx-js. Script handles: chapter headings (H1, centered), section headings (H2, bold), subsection headings (H3, bold italic), body paragraphs (12pt EB Garamond, double-spaced / 480 twip line spacing), placeholder text (centered, italic, gray), scene breaks (centered asterisks), inline bold/italic, and centered bottom page numbers via Footer. Page size: 5.5"×8.5" (7920×12240 DXA). Margins: 0.875" all sides (1260 DXA). This pipeline worked cleanly for 6 chapters with no rendering failures.
