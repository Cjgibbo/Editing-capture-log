---
date: 2026-09-21
category: edge-case
tier: 3
destination: build-log
summary: "Font conversion pipeline: fontsource npm → woff2 → fonttools/brotli → ttf."
---

# Font conversion pipeline: fontsource npm → woff2 → fonttools/brotli → ttf.

**Tier:** 3
**Destination:** build-log

## Detail

Crimson Pro and Montserrat are available via @fontsource/crimson-pro and @fontsource/montserrat npm packages, which contain woff2 files. The fonttools Python package with brotli decompressor converts woff2 to ttf: font = TTFont('file.woff2'); font.flavor = None; font.save('file.ttf'). EB Garamond is available via apt-get install fonts-ebgaramond. The converted ttf files are used only in the build environment — the .docx references font names and requires the fonts installed on the rendering machine.
