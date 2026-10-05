---
date: 2026-09-12
category: format
tier: 2
destination: build-log
summary: "LibreOffice PDF conversion outputs to working directory root, not the source file's directory."
---

# LibreOffice PDF conversion outputs to working directory root, not the source file's directory.

**Tier:** 2
**Destination:** build-log

## Detail

soffice --convert-to pdf output/chapter-01.docx writes the PDF to the current working directory (/home/claude/chapter-01.pdf), not to /home/claude/output/chapter-01.pdf. The subsequent pdftoppm command failed when looking for output/chapter-01.pdf. Fix: reference the PDF at the working directory root, or cd into the output directory before converting.
