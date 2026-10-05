---
date: 2026-09-14
category: edge-case
tier: 3
destination: build-log
summary: "Mid-chapter full-page elements (diagrams, images) create pagination segments the opener vertical drop cannot reach."
---

# Mid-chapter full-page elements (diagrams, images) create pagination segments the opener vertical drop cannot reach.

**Tier:** 3
**Destination:** build-log

## Detail

Chapter 1 has two full-page diagram insertions mid-chapter. These diagrams force page breaks that segment the text flow into before-diagram and after-diagram blocks. Increasing the opener vertical drop only affects text before the first diagram — it cannot push lines past a diagram page break. The 3 orphan lines at the end of Ch 1 are in the after-second-diagram segment. Fixing this requires post-diagram spacing adjustment — adding padding after the diagram page break to push those trailing lines backward. This is a separate mechanism from the opener drop and needs its own implementation for the standalone app.
