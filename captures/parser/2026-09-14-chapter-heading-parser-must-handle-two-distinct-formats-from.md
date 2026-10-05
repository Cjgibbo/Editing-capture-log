---
date: 2026-09-14
category: parser
tier: 3
destination: build-log
summary: "Chapter heading parser must handle two distinct formats from Tier 2 output files."
---

# Chapter heading parser must handle two distinct formats from Tier 2 output files.

**Tier:** 3
**Destination:** build-log

## Detail

Chapters 1–6 came through as single-line headings: **CHAPTER N: Title**. Chapters 7–11 came through as split headings: **CHAPTER N** on one line, **Title** on the next non-empty line. The parser regex ^\*\*CHAPTER\s+(\d+):\s*(.+?)\*\*$ only catches format 1. A second regex ^\*\*CHAPTER\s+(\d+)\*\*$ catches format 2 and triggers a lookahead for the title on the next bold line. Both formats must be supported — the Tier 2 output format is not guaranteed consistent across batches.
