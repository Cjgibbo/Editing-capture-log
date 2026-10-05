---
date: 2026-09-12
category: format
tier: 2
destination: build-log
summary: "Bash brace expansion does not work with /bin/sh — use explicit file lists instead."
---

# Bash brace expansion does not work with /bin/sh — use explicit file lists instead.

**Tier:** 2
**Destination:** build-log

## Detail

wc -w /home/claude/chapters/chapter-0{1,2,3}.md failed because the container's /bin/sh doesn't expand braces. The command was interpreted as a single literal filename. Fix: list each file explicitly or use a glob pattern that sh supports.
