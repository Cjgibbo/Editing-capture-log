---
date: 2026-09-12
category: edge-case
tier: 2
destination: build-log
summary: "Prost championship count error was deeper than the Tier 1 handoff identified — 1987 was Piquet's title, not Prost's."
---

# Prost championship count error was deeper than the Tier 1 handoff identified — 1987 was Piquet's title, not Prost's.

**Tier:** 2
**Destination:** build-log

## Detail

Tier 1 handoff flagged that Ch 6 and Ch 8 said Prost won 1988 (should be Senna). During Tier 2 read, discovered Ch 6 also lists Prost as "Three-time world champion (1985, 1986, 1987)" — but 1987 was Nelson Piquet's championship. Prost had two titles pre-1988, not three. This compounded the 1988 error: Ch 6 said "Prost: 1988 World Champion (his 3rd title)" which was wrong on both the year and the count. Additionally, Ch 8 contradicted itself internally — stated Prost won 1988 by 11 points, then later credited Senna with three titles including 1988. Resolution: corrected all championship references across Ch 6 and Ch 8 to match historical record. Lesson: when a factual error is flagged, check the surrounding facts in the same passage — errors cluster.
