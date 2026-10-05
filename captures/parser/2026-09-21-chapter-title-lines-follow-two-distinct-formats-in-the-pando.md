---
date: 2026-09-21
category: parser
tier: 3
destination: build-log
summary: "Chapter title lines follow two distinct formats in the pandoc markdown output."
---

# Chapter title lines follow two distinct formats in the pandoc markdown output.

**Tier:** 3
**Destination:** build-log

## Detail

Chapters 1–6: **CHAPTER N: Title** — combined on one line, sometimes with em-dash subtitle (e.g., **CHAPTER 2: The Heart of the Beast --- Engines**).

Chapters 7–11: **CHAPTER N** then blank line then **Title** — split across lines.

Parser must handle both: check for title text after the colon on the CHAPTER line, and if absent, look for a standalone bold line on the next non-blank line.
