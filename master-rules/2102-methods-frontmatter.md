---
description: "ENFORCE frontmatter standards for all content within the 'Methods' directory."
globs: ["**/Methods/**"]
alwaysApply: false
---
# Methods Directory Frontmatter

All files within any `Methods` directory (e.g., `Core/Controllers/Methods/`) **MUST** adhere to the following frontmatter standards.

## Required Fields
- `domain`: Must be `methods`.
- `type`: Must be one of the approved types for method notes (e.g., `guide`, `procedure`, etc).
- `tags`: Must be `notes-active`.
- `subject`: Must be the current system level entity.

## Frontmatter by Example

### For a Guide
Use for files that provide step-by-step instructions or best practices.

```yaml
---
type: guide
domain: methods
subject: General | [Project Name] | [Lens Name]
status: draft
tags: notes-active
summary: "A guide detailing the process for [specific task]."
---
```

### For a Procedure
Use for files that outline a formal, repeatable process.

```yaml
---
type: procedure
domain: methods
subject: General | [Project Name] | [Lens Name]
status: finalized
tags: notes-active
summary: "A formal procedure for executing [specific workflow]."
---
```
