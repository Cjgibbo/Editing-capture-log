---
date: 2026-09-12
category: format
tier: 2
destination: build-log
summary: "Editorial review format spec implemented in docx generation code."
---

# Editorial review format spec implemented in docx generation code.

**Tier:** 2
**Destination:** build-log

## Detail

Page setup for all editorial review chapters:

	•	Page size: 7920 × 12240 DXA (5.5" × 8.5")

	•	Margins: 1440 DXA all sides (1")

	•	Line spacing: 480 (double)

	•	Body font: EB Garamond, 24 half-points (12pt)

	•	Section headings: EB Garamond bold, 24 half-points

	•	Part headings: EB Garamond bold, 26 half-points

	•	Chapter title: EB Garamond bold, 36 half-points, centered

	•	Page numbers: centered bottom footer using PageNumber.CURRENT

	•	First-line indent: 720 DXA (0.5") on body paragraphs; opening paragraphs of sections use noIndent

	•	NumberFormat.DECIMAL for page numbering

EB Garamond is not installed on the server's LibreOffice, so PDF verification renders in a sans-serif fallback. The font specification is correct in the .docx XML and renders properly when opened on a system with the font.
