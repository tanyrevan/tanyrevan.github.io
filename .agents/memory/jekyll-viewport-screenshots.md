---
name: Jekyll viewport screenshots
description: Avoid noisy Jekyll watcher rebuilds during local Chromium viewport checks.
---

When taking screenshots with headless Chromium in this workspace, set `--user-data-dir` to a temporary directory outside the project. The default Chromium profile writes cache and state files under the workspace, which Jekyll's watcher notices and can trigger repeated rebuilds.

**Why:** A responsive-preview check caused Jekyll to regenerate for many browser profile files, obscuring the useful build output even though the site continued serving normally.

**How to apply:** For Chromium-based viewport tests while `jekyll serve` is running, pass a unique `/tmp/...` profile directory and remove it after the check if appropriate.