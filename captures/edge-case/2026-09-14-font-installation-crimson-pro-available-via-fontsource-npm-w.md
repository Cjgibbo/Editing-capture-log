---
date: 2026-09-14
category: edge-case
tier: 3
destination: build-log
summary: "Font installation: Crimson Pro available via fontsource npm → woff2 → ttf conversion; EB Garamond via apt fonts-ebgaramond; Montserrat via raw.githubusercontent.com direct download."
---

# Font installation: Crimson Pro available via fontsource npm → woff2 → ttf conversion; EB Garamond via apt fonts-ebgaramond; Montserrat via raw.githubusercontent.com direct download.

**Tier:** 3
**Destination:** build-log

## Detail

GitHub raw.githubusercontent.com returns 404 for EB Garamond TTF files (repo structure changed). The apt package fonts-ebgaramond works and installs to /usr/share/fonts/truetype/ebgaramond/. Font names in the system: EB Garamond 12 (Regular, Bold, Italic), EB Garamond SC 12. Montserrat downloads successfully from raw.githubusercontent.com/JulietaUla/montserrat/master/fonts/ttf/. Crimson Pro requires: npm pack @fontsource/crimson-pro → extract tgz → convert woff2 to ttf using fontTools (pip install fonttools brotli). Font family name after conversion: Crimson Pro.
