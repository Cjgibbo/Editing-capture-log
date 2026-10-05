---
date: 2026-09-15
category: parser
tier: 3
destination: build-log
summary: "Chapter heading parser must handle two distinct formats from Tier 2 output."
---

# Chapter heading parser must handle two distinct formats from Tier 2 output.

**Tier:** 3
**Destination:** build-log

## Detail

Chapters 1–6 use single-line format: CHAPTER 1: What Makes an F1 Car Impossible

Chapters 7–11 use split-line format:

CHAPTER 7

Mind, Body, Spirit

const singleMatch = headerLine.match(/^CHAPTER\s+(\d+)\s*:\s*(.+)$/i);

const splitMatch = headerLine.match(/^CHAPTER\s+(\d+)\s*$/i);

For split format, skip blank lines after line 1, take next non-blank as title, set bodyStart accordingly. Without this fix, chapterNum defaults to 0 and chapterTitle grabs the raw header line, producing "Chapter 0: CHAPTER 7" in the TOC.
