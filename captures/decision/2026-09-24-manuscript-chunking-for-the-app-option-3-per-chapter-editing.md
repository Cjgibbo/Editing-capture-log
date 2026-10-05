---
date: 2026-09-24
category: decision
tier: general
destination: build-log
summary: "Manuscript chunking for the app = Option 3 (per-chapter editing + a manuscript-wide consistency map), structured as a three-phase job."
---

# Manuscript chunking for the app = Option 3 (per-chapter editing + a manuscript-wide consistency map), structured as a three-phase job.

**Tier:** general
**Destination:** build-log

## Detail

Rejected whole-manuscript-single-call (Option 1) not mainly on cost but on unpredictability — it works for small books and silently fails on large ones (150k+), and you can't know which bucket a paying customer lands in ahead of time. Rejected plain per-chapter (Option 2) because it can't catch cross-chapter inconsistencies (name spellings, grey/gray) that the Tier 1 spec requires standardizing. Option 3 runs identically at any manuscript size — same code path, more chapters through the loop. Three phases: (1) map pass — one whole-manuscript read builds the consistency map (canonical spellings, style choices, name registry); this is a small MODEL call, not pure code, because canonical-choice selection is a judgment call, not a lookup; (2) edit pass — per chapter, map rides along as a few hundred extra input tokens, does the T1/T2 work; (3) assemble — stitch outputs, generate briefing. Cost premium over plain per-chapter is small (map is a few hundred lines; the extra read is once per job, not per chapter) and is halved again by batch. Rationale for accepting the premium: consistency, quality, readability, customer care rank above marginal token savings. OPEN (Track B, pending real books): when a chapter arrives after the map is built (batched-arrival case the T1 spec allows), does the map rebuild or does the new chapter inherit + flag new items? Frequency of dribbled-in vs. all-at-once arrivals will inform this.
