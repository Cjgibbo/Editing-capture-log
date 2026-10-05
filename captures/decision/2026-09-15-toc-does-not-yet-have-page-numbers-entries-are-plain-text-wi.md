---
date: 2026-09-15
category: decision
tier: 3
destination: build-log
summary: "TOC does not yet have page numbers — entries are plain text without references."
---

# TOC does not yet have page numbers — entries are plain text without references.

**Tier:** 3
**Destination:** build-log

## Detail

The current TOC lists Dedication, Foreword, and all 11 chapters with titles, but no page numbers. Adding page numbers requires either: (a) Word TOC field codes that auto-update (needs LibreOffice to "Update Fields" which may not happen during headless PDF export), (b) post-render page number injection by reading the PDF's page breaks and writing numbers back into the DOCX, or (c) manual calculation. This is an open item for the next revision or the standalone app. Chris's friend may flag this.
