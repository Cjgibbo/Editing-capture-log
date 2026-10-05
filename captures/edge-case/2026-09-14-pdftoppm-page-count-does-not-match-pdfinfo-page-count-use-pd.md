---
date: 2026-09-14
category: edge-case
tier: 3
destination: build-log
summary: "pdftoppm page count does not match pdfinfo page count — use pdfinfo for accurate totals."
---

# pdftoppm page count does not match pdfinfo page count — use pdfinfo for accurate totals.

**Tier:** 3
**Destination:** build-log

## Detail

pdftoppm with -r 72 generated 200+ JPEG files for a 99-page PDF (later 102–103 pages). The file count from ls *.jpg | wc -l is not a reliable page count. pdfinfo <file> | grep Pages returns the correct page count. Use pdfinfo for page count reporting, pdftoppm only for rendering specific page ranges for visual verification.
