---
date: 2026-09-15
category: format
tier: 3
destination: build-log
summary: "Foreword title should be a single line — not the two-line chapter format."
---

# Foreword title should be a single line — not the two-line chapter format.

**Tier:** 3
**Destination:** build-log

## Detail

The build script was outputting both "FOREWORD" (13pt Montserrat Light, mimicking the "CHAPTER ONE" label) and "Foreword" (24pt Montserrat Bold, mimicking the chapter title). Chris flagged "the forward has a subtitle both of them are reading forward." Fix: single "Foreword" line at 24pt Montserrat Bold. The foreword is not a chapter and should not use the chapter heading format.
