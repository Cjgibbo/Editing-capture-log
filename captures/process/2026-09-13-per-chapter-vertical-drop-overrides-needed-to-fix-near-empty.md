---
date: 2026-09-13
category: process
tier: 3
destination: build-log
summary: "Per-chapter vertical drop overrides needed to fix near-empty last pages; global drop alone is insufficient; diagram pages create pagination segments the opener drop can't reach."
---

# Per-chapter vertical drop overrides needed to fix near-empty last pages; global drop alone is insufficient; diagram pages create pagination segments the opener drop can't reach.

**Tier:** 3
**Destination:** build-log

## Detail

Production rules established: (1) keepNext: true on all section/sub headings prevents orphan headers. (2) widowControl: true on all body paragraphs prevents widow lines. (3) Default chapter opener vertical drop set to 4.0" from top edge. (4) Per-chapter drop overrides stored in CH_DROP_OVERRIDE map for chapters whose last page has fewer than ~8 content lines. (5) LibreOffice caps large spaceBefore values on section-first paragraphs — split into multiple spacer paragraphs at max 1.5" each. (6) Chapters with mid-chapter full-page elements (diagrams, images) have paginated segments that the opener drop cannot reach — these need post-element spacing adjustment as a separate mechanism.
