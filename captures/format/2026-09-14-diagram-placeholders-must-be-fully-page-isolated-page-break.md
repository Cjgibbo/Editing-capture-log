---
date: 2026-09-14
category: format
tier: 3
destination: build-log
summary: "Diagram placeholders must be fully page-isolated — page break before AND after."
---

# Diagram placeholders must be fully page-isolated — page break before AND after.

**Tier:** 3
**Destination:** build-log

## Detail

Initial implementation only had pageBreakBefore on the diagram paragraph. Text from the following section flowed onto the diagram page below the caption. Fix: add a trailing pageBreakBefore empty paragraph after the caption to force subsequent text to a new page. Same structure applies when actual images replace placeholders — the image, caption, and trailing break are a unit.
