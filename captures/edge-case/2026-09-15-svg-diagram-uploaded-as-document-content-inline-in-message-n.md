---
date: 2026-09-15
category: edge-case
tier: 3
destination: build-log
summary: "SVG diagram uploaded as document content (inline in message), not as a file on disk — must be written to disk before conversion."
---

# SVG diagram uploaded as document content (inline in message), not as a file on disk — must be written to disk before conversion.

**Tier:** 3
**Destination:** build-log

## Detail

The diagram-5g-force.svg appeared in the uploads list but didn't land at /mnt/user-data/uploads/diagram-5g-force.svg. The SVG content was delivered inline in a <documents> block. Fix: write the SVG content to /home/claude/images/diagram-5g-force.svg manually, then convert to PNG via cairosvg.svg2png(). The previous thread's container had this file already converted — it doesn't carry over between threads.
