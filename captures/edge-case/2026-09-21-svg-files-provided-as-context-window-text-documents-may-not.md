---
date: 2026-09-21
category: edge-case
tier: 3
destination: build-log
summary: "SVG files provided as context-window text documents may not exist on disk."
---

# SVG files provided as context-window text documents may not exist on disk.

**Tier:** 3
**Destination:** build-log

## Detail

The 5g-force.svg appeared in the uploaded_files list and its content was visible in the context window as an <document> block, but the file did not exist at /mnt/user-data/uploads/5g-force.svg. The three JPG files did exist on disk. Had to recreate the SVG from the context text and convert to PNG via cairosvg. ImageMagick's convert delegates SVG to rsvg-convert, which was not installed.
