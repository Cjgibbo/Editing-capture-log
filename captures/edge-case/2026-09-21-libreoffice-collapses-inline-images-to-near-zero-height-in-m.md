---
date: 2026-09-21
category: edge-case
tier: 3
destination: build-log
summary: "LibreOffice collapses inline images to near-zero height in multi-section .docx documents — Word renders them correctly."
---

# LibreOffice collapses inline images to near-zero height in multi-section .docx documents — Word renders them correctly.

**Tier:** 3
**Destination:** build-log

## Detail

Isolated single-section test doc with identical page size (5.5×8.5), margins, section type (ODD_PAGE), titlePage: true, and footer configuration renders images perfectly in LibreOffice. Full book with 16+ sections (front matter + 11 chapters) collapses all four images to ~1px height in LibreOffice rendering. The .docx XML is correct in both cases (identical EMU values). This is a LibreOffice multi-section rendering bug, not a file defect. Word renders the same full-book file correctly.

Implication for pipeline: cannot rely on LibreOffice PDF conversion for visual verification of images in multi-section documents. Text/layout verification is still valid.
