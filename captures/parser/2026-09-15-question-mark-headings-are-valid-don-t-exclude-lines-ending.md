---
date: 2026-09-15
category: parser
tier: 3
destination: build-log
summary: "Question-mark headings are valid — don't exclude lines ending in "?" from heading detection."
---

# Question-mark headings are valid — don't exclude lines ending in "?" from heading detection.

**Tier:** 3
**Destination:** build-log

## Detail

Initial tightening excluded ? endings. This broke "What Is Grip, Anyway?" in Ch 3, which is a real heading. Removed ? from the exclusion list. Headings can be questions. The remaining exclusions (., ,, !, :) are correct — sentences end in periods and commas; exclamation marks and colons at the end of a line almost always indicate body text, not a heading title.
