---
date: 2026-09-12
category: process
tier: 2
destination: build-log
summary: "Verification workflow for docx output: soffice → pdftoppm → view."
---

# Verification workflow for docx output: soffice → pdftoppm → view.

**Tier:** 2
**Destination:** build-log

## Detail

After generating each .docx:

python scripts/office/soffice.py --headless --convert-to pdf chapter.docx --outdir /home/claude/

pdftoppm -jpeg -r 100 chapter.pdf /home/claude/ch-page

Then view on page-01.jpg (first page) and the last page (ending/closing). Spot-checked specific pages when verifying structural changes (e.g., confirming "The Cost" section absent from Ch 7, confirming 1988 fix in Ch 8). Also ran pandoc -t plain + grep for targeted text verification. This workflow caught no rendering issues across five chapters — all rendered clean on first pass.
