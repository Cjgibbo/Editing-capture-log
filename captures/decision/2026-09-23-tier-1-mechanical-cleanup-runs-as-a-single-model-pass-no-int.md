---
date: 2026-09-23
category: decision
tier: 1
destination: build-log
summary: "Tier 1 mechanical cleanup runs as a single-model pass — no internal cheap-pass/smart-pass split."
---

# Tier 1 mechanical cleanup runs as a single-model pass — no internal cheap-pass/smart-pass split.

**Tier:** 1
**Destination:** build-log

## Detail

On the standalone-app batch pipeline (24–48hr SLA, prompt caching on the static prefix), the cost case for splitting Tier 1 into a cheap raw grammar pass plus a smarter consistency/flagging pass disappears — a capable model at 50% batch + cached input is already cheap enough that the second call adds cost and a failure point for no gain. Decision: one model, one mechanical pass for Tier 1. Stable regardless of whether Tier 1 stands alone or passes off to Tier 2.
