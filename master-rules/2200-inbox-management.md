---
description: "ENFORCE strict inbox management standards for content capture and processing, including naming, frontmatter, and workflow."
globs: ["**/0. Inbox/**", "**/inbox/**"]
alwaysApply: false
---
# Inbox Management Directives

## Input Processing (Adding to Inbox)

- **USE** timestamp-based naming: `YYYY-MM-DD_HHMM_descriptive-name.md`.
- **APPLY** all required frontmatter fields correctly.
- **MAINTAIN** atomicity of insights in each file.
- **PROCESS** conversational transcripts systematically and sequentially, without echoing the source.

## Content Processing (Working with Inbox)

### Required Frontmatter

- **VALIDATE** that all inbox files contain the following frontmatter:
  - `type: capture`
  - `domain: inbox`
  - `domain-category`: (Must be one of: `raw-insight`, `project-idea`, `feedback`, `external-knowledge`, `method-improvement`, `question`, `anomaly`)
  - `status: new`
  - `subject`: (`General` or Project-specific)
  - `summary`: (Brief, accurate description)

### Processing & Structure

- **FOLLOW** the Insight Cultivation and Inbox Management guides for processing paths.
- **ENSURE** all content has a clear conceptual foundation, with technical details included only when relevant and valuable.
- **STRUCTURE** content with clear, atomic insights and provide source context where applicable.