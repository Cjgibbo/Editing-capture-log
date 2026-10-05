---
date: 2026-09-14
category: format
tier: 3
destination: build-log
summary: "Diagram caption escapes: pandoc outputs \", \', \\, and --- in caption text that must be cleaned before rendering."
---

# Diagram caption escapes: pandoc outputs \", \', \\, and --- in caption text that must be cleaned before rendering.

**Tier:** 3
**Destination:** build-log

## Detail

The diagram placeholder regex captures the caption including pandoc escape sequences. Example raw caption: Speed Comparison --- \"The Race: 0 to 100 MPH\". Must apply full cleanText(): replace \\" → ", \\' → ', --- → —, --- → —, -- → –, \\\\ → empty. This was missed in the initial implementation and produced visible triple-hyphens and backslash-quotes in captions.
