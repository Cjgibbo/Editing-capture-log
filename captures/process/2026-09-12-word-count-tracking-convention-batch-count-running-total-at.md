---
date: 2026-09-12
category: process
tier: 2
destination: build-log
summary: "Word count tracking convention — batch count + running total at each delivery."
---

# Word count tracking convention — batch count + running total at each delivery.

**Tier:** 2
**Destination:** build-log

## Detail

Format used: "Batch word count: ~X,XXX | Running total (Ch 1–N): ~XX,XXX" after each chapter delivery. Word counts pulled via pandoc -t plain file.docx | wc -w. Ch 1–6 running total (~11,540) came from the handoff. Ch 7–11 counts: Ch 7 ~2,230; Ch 8 ~2,220; Ch 9 ~2,382; Ch 10 ~2,028; Ch 11 ~2,585. Final total: ~22,985. These counts are from the clean output files, not the originals — voice conversion and bullet-to-prose change word counts from the source.
