---
description: "COMMAND: Use `YYYY-MM-DD_HHMM-description.md` for all new Inbox files and apply the standard `type: capture` frontmatter."
globs: ["**/inbox/**", "**/0. Inbox/**"]
alwaysApply: false
---
# Inbox File Naming Protocol

- **WHEN CREATING A NEW INBOX FILE:**
  1.  **FETCH a system timestamp:** `date +%Y-%m-%d_%H%M`.
  2.  **CONSTRUCT the filename:** `[TIMESTAMP]-kebab-case-description.md`.
  3.  **APPLY** the standard `type: capture` frontmatter:


```yaml
---
type: capture
domain: inbox
subject: [`General`, `[Project Name]`, or `[Lens Name]`]
status: new
summary: "Brief note on what was captured and why."
---
```