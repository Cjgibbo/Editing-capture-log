---
date: 2026-09-15
category: parser
tier: 3
destination: build-log
summary: "Heading false-positive guard — tightened heuristic to prevent opening paragraphs from being styled as headings."
---

# Heading false-positive guard — tightened heuristic to prevent opening paragraphs from being styled as headings.

**Tier:** 3
**Destination:** build-log

## Detail

Chapter 3 opens with "Here's something that sounds like a lie but isn't:" — short, title-case start, no period. The original parser caught it as a sub-heading. Fix: exclude lines that end in ?, !, : (later revised: allow ? since headings can be questions like "What Is Grip, Anyway?"), exclude lines starting with common sentence-opener words (Here, Some, Imagine, Every, Close, Rain), and exclude lines containing .  mid-text (sentence indicator). The guard list will need expansion as new manuscripts surface different opening patterns.
