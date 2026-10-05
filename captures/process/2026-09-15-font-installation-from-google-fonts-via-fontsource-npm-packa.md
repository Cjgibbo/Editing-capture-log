---
date: 2026-09-15
category: process
tier: 3
destination: build-log
summary: "Font installation from Google Fonts via fontsource npm packages, converted from woff2 to ttf with fontTools."
---

# Font installation from Google Fonts via fontsource npm packages, converted from woff2 to ttf with fontTools.

**Tier:** 3
**Destination:** build-log

## Detail

Crimson Pro and Montserrat installed via @fontsource/crimson-pro and @fontsource/montserrat npm packages. woff2 files converted to ttf using fontTools.ttLib.TTFont with flavor = None. Installed to /usr/local/share/fonts/ and registered with fc-cache -f. Specific weights needed: Crimson Pro 400/400i/600/700/700i, Montserrat 300/400/500/600/700. No client font upload needed — both are Google Fonts.
