---
description: "ENFORCE frontmatter standards for all content within 'Inbox' directories."
globs: ["**/0. Inbox/**", "**/inbox/**"]
alwaysApply: false
---
# Inbox Frontmatter

All new files created in an `Inbox` directory **MUST** use the following frontmatter structure.

## Required Fields
- `type`: Must be `capture`.
- `domain`: Must be `inbox`.
- `status`: Must be `new`.
- `tags`: Must be `notes-active`.
- `subject`: Must be the current system level entity.

## Example Inbox Frontmatter

```yaml
---
type: capture
domain: inbox
domain-category: raw-insight | project-idea | feedback | external-knowledge | method-improvement | question | anomaly
status: new
tags: notes-active
subject: General | [Project Name] | [Lens Name]
summary: "A concise summary of the captured content."
---
```
