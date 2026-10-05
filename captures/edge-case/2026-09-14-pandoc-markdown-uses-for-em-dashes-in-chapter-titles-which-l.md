---
date: 2026-09-14
category: edge-case
tier: 3
destination: build-log
summary: "Pandoc markdown uses --- for em dashes in chapter titles, which leaks into rendered output if not cleaned."
---

# Pandoc markdown uses --- for em dashes in chapter titles, which leaks into rendered output if not cleaned.

**Tier:** 3
**Destination:** build-log

## Detail

Pandoc converts em dashes to --- (space-hyphen-hyphen-hyphen-space) in markdown output. The inline text parser was cleaning these in body text, but the chapter title was being passed directly to the TextRun without cleanup. Chapter 2 rendered as "The Heart of the Beast --- Engines" instead of "The Heart of the Beast — Engines". Fix: apply cleanText() to chapter titles, section headings, sub-headings, and diagram captions — every text path, not just body paragraphs. Same applies to escaped quotes (\\", \\') and brackets (\[, \]).
