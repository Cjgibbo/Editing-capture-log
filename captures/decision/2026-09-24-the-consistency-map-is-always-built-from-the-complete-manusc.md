---
date: 2026-09-24
category: decision
tier: general
destination: build-log
summary: "The consistency map is always built from the complete manuscript — enforced by an intake-closed gate, not by map-rebuild logic."
---

# The consistency map is always built from the complete manuscript — enforced by an intake-closed gate, not by map-rebuild logic.

**Tier:** general
**Destination:** build-log

## Detail

Resolves the batched-arrival open item from the chunking decision. Governing rule: the map is always built from the complete manuscript, no exceptions. Before-the-fact this means the map pass (phase 1) does not run until intake is closed — an explicit operator "manuscript complete, start processing" signal triggers it. Files landing in the inbox folder accumulate but do not auto-start a job; arrival is not a trigger, operator confirmation is. This is the app version of the current system's Tier 1 question "Ready for the briefing, or uploading more chapters?" — same human gate, different UI (a button). Because processing can't start mid-arrival, the batched-arrival case needs no rebuild logic at all. The only genuine after-the-fact case is a chapter arriving AFTER the operator hit go and the job ran — treated as a late addition/correction, handled by the operator re-running the job on the complete set (rare, human-judged, no special automation). "Rebuild the map" and "don't build until complete" are the same rule from two sides: map = complete manuscript, always; both behaviors fall out of enforcing that one invariant.
