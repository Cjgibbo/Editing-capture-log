---
date: 2026-09-14
category: parser
tier: 3
destination: build-log
summary: "Foreword and dedication text must be joined into paragraphs before rendering — pandoc line wraps are not paragraph breaks."
---

# Foreword and dedication text must be joined into paragraphs before rendering — pandoc line wraps are not paragraph breaks.

**Tier:** 3
**Destination:** build-log

## Detail

Pandoc wraps markdown output at ~72 characters. Each wrapped line appears as a separate line in the markdown. If each line is rendered as its own paragraph, the foreword renders as a stair-step of indented fragments instead of flowing text. Fix: use the same paragraph-joining logic as the chapter parser — accumulate continuation lines (non-empty, non-heading) into a single paragraph string before creating the docx paragraph. This applies to all front/back matter text parsed from docx via pandoc.
