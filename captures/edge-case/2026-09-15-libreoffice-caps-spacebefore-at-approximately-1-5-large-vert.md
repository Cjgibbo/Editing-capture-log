---
date: 2026-09-15
category: edge-case
tier: 3
destination: build-log
summary: "LibreOffice caps spaceBefore at approximately 1.5" — large vertical drops must be split into multiple spacer paragraphs."
---

# LibreOffice caps spaceBefore at approximately 1.5" — large vertical drops must be split into multiple spacer paragraphs.

**Tier:** 3
**Destination:** build-log

## Detail

A single spaceBefore of 3.0" or more renders as ~1.5" max in LibreOffice PDF export. Fix: split into multiple paragraphs each with spaceBefore of ~1.4". Copyright page uses 3 × 1.4" spacers. Chapter drops use 2 × 1.4" spacers. Title page uses a single 2.5" spacer (under the cap). This was documented in the previous thread's handoff but the rebuilt script initially used single large spacers and had to be corrected.
