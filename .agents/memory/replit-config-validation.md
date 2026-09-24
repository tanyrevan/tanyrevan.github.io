---
name: Replit config edits
description: Replit-managed TOML configuration requires validated replacement.
---

Treat `.replit` as managed configuration. Direct file edits may be rejected even when other project files can be patched normally.

**Why:** Replit validates runtime, deployment, and workflow configuration separately from ordinary source files.

**How to apply:** Write the complete intended TOML to a temporary file inside the workspace, then call `verifyAndReplaceDotReplit` with that file path. Artifact-owned workflows are managed with their artifacts rather than the generic workflow-removal callback.