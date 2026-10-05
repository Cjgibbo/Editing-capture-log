---
date: 2026-09-15
category: edge-case
tier: 3
destination: build-log
summary: "Backslash-ellipsis bug was introduced by build script, not present in source files."
---

# Backslash-ellipsis bug was introduced by build script, not present in source files.

**Tier:** 3
**Destination:** build-log

## Detail

Chris flagged sound\… in the rendered PDF. Checked all 11 chapter .docx files and the foreword via pandoc -t plain --wrap=none | grep '\\' — zero backslashes in any source. The escape character was introduced somewhere in the text processing pipeline of the previous thread's build script. Fix in cleanText(): .replace(/\\/g, "") strips all stray backslashes from every text path (body, titles, captions, headings). Must be applied universally — the previous build's bug was that cleanText() wasn't applied to all text paths.
