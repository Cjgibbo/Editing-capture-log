---
date: 2026-09-14
category: decision
tier: 3
destination: style-reference
summary: "Crimson Pro replaces EB Garamond as the body font in the Stride template for lining figures."
---

# Crimson Pro replaces EB Garamond as the body font in the Stride template for lining figures.

**Tier:** 3
**Destination:** style-reference

## Detail

EB Garamond 12 (apt package) renders old-style (lowercase) numerals by default. For manuscripts with heavy technical numbers (RPMs, G-forces, speeds, lap counts), old-style figures look busy and scan poorly. Crimson Pro is the replacement — same classic serif feel, lining figures, available via fontsource npm package (woff2 → ttf conversion via fontTools). Lora was also tested and available but Crimson Pro is closer to EB Garamond's character. The Stride template spec in memory has been updated to reflect this. EB Garamond remains the default for templates where old-style figures are appropriate (Heritage, Vespers, Chronicle).
