---
date: 2026-09-15
category: process
tier: 3
destination: build-log
summary: "Page numbers solved via python-docx post-processing — the npm docx library cannot be relied on for footers."
---

# Page numbers solved via python-docx post-processing — the npm docx library cannot be relied on for footers.

**Tier:** 3
**Destination:** build-log

## Detail

After the Node.js build script generates the DOCX, a Python script (add-page-numbers.py) opens it with python-docx and injects PAGE field codes into footers for sections 4+ (foreword and chapters). Uses fldChar begin → instrText PAGE → fldChar end pattern. Sets different_first_page_header_footer = True on chapter sections to suppress page numbers on openers. Sets is_linked_to_previous = False on each footer to prevent inheritance from front matter sections. This two-stage pipeline (Node.js build → Python post-process) is the reliable pattern for the standalone app.
