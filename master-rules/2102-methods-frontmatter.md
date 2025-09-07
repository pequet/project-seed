---
type: overview
domain: system-state
subject: Seed Project
description: "ENFORCE frontmatter standards for all content within the 'Methods' directory."
globs: ["**/Methods/**"]
alwaysApply: false
---
# 2102: Methods Frontmatter (and Guides in /Guides)

This rule enforces consistent frontmatter for Methods and Guides under `Controllers/Methods/`.

- Methods (any file under `Controllers/Methods/**`):
  - Must have `domain: methods`

- Guides (any file under `Controllers/Methods/Guides/**`):
  - Must have `type: guide`

Notes:
- Guides explain how-to within rule constraints; they do not override norms.
- Methods define operational practices and must live under `Controllers/Methods/`.
