---
date: 2026-09-14
category: decision
tier: 3
destination: style-reference
summary: "Chapter opener vertical drop increased to 4.0" default, with per-chapter overrides for near-empty last pages."
---

# Chapter opener vertical drop increased to 4.0" default, with per-chapter overrides for near-empty last pages.

**Tier:** 3
**Destination:** style-reference

## Detail

Chris prefers chapter openers starting lower on the page — mid-page or below. Default vertical drop set to 4.0" from top edge (was 2.5" per original Stride spec). Per-chapter overrides stored in CH_DROP_OVERRIDE map, keyed by chapter number, for chapters whose last page has fewer than ~8 content lines. Chris's language: "I don't have a problem with the beginning of a chapter starting lower in order to keep the last page of a chapter from only having a couple of sentences." Consistency across chapters is fine as long as it doesn't create near-empty last pages. The 4.0" default applies to the Stride template specifically — other templates retain their own spec values unless Chris requests the same treatment.
