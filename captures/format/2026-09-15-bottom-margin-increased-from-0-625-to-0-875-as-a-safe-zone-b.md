---
date: 2026-09-15
category: format
tier: 3
destination: style-reference
summary: "Bottom margin increased from 0.625" to 0.875" as a safe zone — body text can never crowd the page number."
---

# Bottom margin increased from 0.625" to 0.875" as a safe zone — body text can never crowd the page number.

**Tier:** 3
**Destination:** style-reference

## Detail

Chris flagged that text was running into the page number area when both sat on the same floor. Solution: increase bottom margin by 0.25" (Option A from the two options presented). const MARGIN_BOTTOM = 0.875 * DXA; // 1260. Applies to all templates. The page number position stays where it is; the text block ends higher.
