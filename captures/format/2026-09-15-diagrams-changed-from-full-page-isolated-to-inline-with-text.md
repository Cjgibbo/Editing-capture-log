---
date: 2026-09-15
category: format
tier: 3
destination: build-log
summary: "Diagrams changed from full-page isolated to inline with text — images scale proportionally from source dimensions."
---

# Diagrams changed from full-page isolated to inline with text — images scale proportionally from source dimensions.

**Tier:** 3
**Destination:** build-log

## Detail

Previous build: page break before and after each diagram, consuming an entire page per image. New build: diagrams flow inline with body text. Image dimensions are read via identify -format '%wx%h' and scaled proportionally to fit within max 4.0" wide × 5.0" tall, preserving aspect ratio. The previous build hardcoded a fixed width×height that distorted portrait-oriented images (all four diagrams are ~1179×1800, roughly 2:3 portrait). Max display area should be generous enough to keep diagrams readable but leave room for text above/below.
