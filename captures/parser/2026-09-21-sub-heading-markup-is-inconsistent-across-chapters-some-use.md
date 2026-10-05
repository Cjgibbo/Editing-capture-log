---
date: 2026-09-21
category: parser
tier: 3
destination: build-log
summary: "Sub-heading markup is inconsistent across chapters — some use bold-italic (*), others use bold ()."
---

# Sub-heading markup is inconsistent across chapters — some use bold-italic (*), others use bold ().

**Tier:** 3
**Destination:** build-log

## Detail

Ch 2: Part headings = **Part 1: ...**, sub-headings = ***What's a Turbocharger?*** (triple-star bold-italic).

Ch 7: Part headings = **Part 1: ...**, sub-headings = **The Brazilian Beach** (double-star bold only).

Parser cannot rely on *** vs ** to distinguish heading levels. Instead: detect Part structure per-chapter, then any non-Part bold-only line under 120 chars = sub-heading (regardless of * count).
