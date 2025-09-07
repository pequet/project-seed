---
type: overview
domain: system-state
subject: Seed Project
description: "Enforce placement for hub pages: any file with type: hub must be located under Views/."
globs: *,**/*
alwaysApply: false
---
# 2105: Hubs Must Live Under Views

This rule enforces that any page declaring `type: hub` is placed under the `Views/` subtree.

- Must
  - If frontmatter contains `type: hub`, the file path must match `**/Views/**`

- Must not
  - Place `type: hub` pages under `Models/**` or `Controllers/**`

