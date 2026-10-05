---
date: 2026-09-21
category: parser
tier: 3
destination: build-log
summary: "Pandoc markdown escape patterns that require cleanup before typesetting."
---

# Pandoc markdown escape patterns that require cleanup before typesetting.

**Tier:** 3
**Destination:** build-log

## Detail

Pandoc .docx → markdown output produces: \' for apostrophes (convert to \u2019 smart apostrophe); \" for double quotes (convert to smart quotes via regex); --- for em dashes (convert to \u2014); -- for en dashes (convert to \u2013); \... for ellipsis (convert to \u2026 or strip backslash); stray backslashes before other characters (strip). The cleanText() function handles all of these.
