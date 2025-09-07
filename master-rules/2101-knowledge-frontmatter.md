---
type: overview
domain: system-state
subject: Seed Project
description: "ENFORCE frontmatter standards for all content within the '2. Knowledge' directory."
globs: **/*Knowledge/*.md,**/*Knowledge/**/*.md
alwaysApply: false
---
# 2101: Knowledge Frontmatter

This rule enforces consistent frontmatter for knowledge notes located under `Models/2. Knowledge/`.

- Must
  - `type: overview` (unless explicitly and locally justified)
  - `domain` ∈ {`concepts`, `patterns`}
  - `type: hub` is not permitted under `Models/2. Knowledge/`
- Should
  - Keep Concepts and Core Patterns co-located; distinguish only via `domain`
  - Use the Dual Knowledge Organization principles to align structural and functional identity

Notes:
- Hubs belong under `Views/`, not in `Models/` or `Controllers/`.
