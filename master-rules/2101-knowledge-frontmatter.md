---
description: "ENFORCE frontmatter standards for all content within the '2. Knowledge' directory."
globs: ["**/2. Knowledge/**"]
alwaysApply: false
---
# Knowledge Directory Frontmatter

All files within the `2. Knowledge` directory and its subdirectories **MUST** adhere to the following frontmatter standards to ensure consistency and proper data processing.

## Required Fields
- `type`: Must be `overview` or `hub`.
- `domain`: Must be either `concepts` or `patterns`.
- `tags`: Must be `notes-active`.
- `subject`: Must be the current system level entity.

## Frontmatter by Example

### Concept 
Use for files that define and explain a fundamental concept.

```yaml
---
type: overview
domain: concepts
subject: General | [Project Name] | [Lens Name]
status: draft
tags: notes-active
summary: "A concise definition and explanation of the concept."
---
```

### Core Pattern 
Use for files that describe a recurring pattern or solution.

```yaml
---
type: overview
domain: patterns
subject: General | [Project Name] | [Lens Name]
status: draft
tags: notes-active
summary: "A description of a recurring pattern, its context, and its application."
---
```
