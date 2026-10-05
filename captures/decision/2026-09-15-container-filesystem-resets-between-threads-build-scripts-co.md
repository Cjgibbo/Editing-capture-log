---
date: 2026-09-15
category: decision
tier: 3
destination: build-log
summary: "Container filesystem resets between threads — build scripts, converted images, and font installations must be reconstructed from handoff notes and project memory."
---

# Container filesystem resets between threads — build scripts, converted images, and font installations must be reconstructed from handoff notes and project memory.

**Tier:** 3
**Destination:** build-log

## Detail

The build script (build-book.js), converted diagram PNG, and installed fonts only existed on the previous thread's container. The handoff file carried enough information to reconstruct the build, but it took significant work. For the standalone app, the build script should be stored in a persistent location (GitHub repo, Google Drive) and the handoff file should include a pointer to it. Project memory's build log served as the reconstruction reference.
