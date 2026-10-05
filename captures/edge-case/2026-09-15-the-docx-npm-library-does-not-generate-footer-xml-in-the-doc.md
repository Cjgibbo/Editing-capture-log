---
date: 2026-09-15
category: edge-case
tier: 3
destination: build-log
summary: "The docx npm library does not generate footer XML in the DOCX output — footers defined in section properties are silently dropped."
---

# The docx npm library does not generate footer XML in the DOCX output — footers defined in section properties are silently dropped.

**Tier:** 3
**Destination:** build-log

## Detail

Footer objects created with new Footer({ children: [...] }) and assigned to section properties.footers.default produce zero <w:footerReference> elements in word/document.xml and zero footer part files in the DOCX archive. Confirmed by inspecting the ZIP contents. This affects both PageNumber.CURRENT inside TextRun.children and SimpleField({ instruction: " PAGE " }) approaches — neither produces output because the footer container itself isn't generated. Library version: docx 9.x (current npm). Root cause unknown — may be a bug or API mismatch.
