---
date: 2026-09-12
category: format
tier: 2
destination: build-log
summary: "Docx generation uses Node.js docx library from scratch rather than editing uploaded file XML."
---

# Docx generation uses Node.js docx library from scratch rather than editing uploaded file XML.

**Tier:** 2
**Destination:** build-log

## Detail

All chapter .docx files were generated fresh using require("docx") rather than unzipping the uploaded .docx and editing word/document.xml. The content was read from the uploads via pandoc -t markdown, then the edited text was structured into the docx library's Paragraph/TextRun API. This approach is cleaner for chapters that need heavy restructuring (voice conversion, bullet-to-prose, section removal/reordering) but means every formatting decision must be explicitly coded — nothing carries over from the original file. Trade-off is acceptable for Tier 2 implementation pass where the content is being substantially reworked.
