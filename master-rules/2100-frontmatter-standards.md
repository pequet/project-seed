---
description: "Enforce strict frontmatter schema for all documents."
globs: ["*.md", "**/*.md"]
alwaysApply: true
---
# Frontmatter Standards

## Prohibited Fields

- NO `title` (use the filename as title)
- NO `category` (use `domain` and `type` instead)
- NO Custom fields not in the standard schema

## Standard `type:` (Choose ONE - NEVER match domain)

- **`overview`** (90% of files): Standard content notes
- **`hub`** (5% of files): Navigation pages that link to related content
- **`guide`**: Instructions and best practices
- **`procedure`**: Step-by-step instructions
- **`framework`**: High-level strategic documents
- **`principles`**: Fundamental rules
- **`application`**: Practical implementations
- **`examples`**: Practical instances
- **`analysis`**: Deep examinations
- **`log`**: Chronological records

## Standard `domain:` (Choose ONE - NEVER match type)

- **`concepts`**: Fundamental knowledge elements (default in Models/2. Knowledge)
- **`patterns`**: Core patterns identified through analysis (second default in Models/2. Knowledge)
- **`methods`**: Procedures and processes (default in Controllers/Methods)
- **`analytical-lenses`**: Analytical perspectives
- **`assets`**: Supporting resources
- **`quotes`**: Direct quotations
- **`system-state`**: Documentation about system state

> [!IMPORTANT]
> **File Organization and the `domain` Field (Dual Knowledge Organization)**:
> The framework employs a "Dual Knowledge Organization" (see Framework Terminology):
> 1.  **Structural Organization**: Files, including those with `domain: concepts` or `domain: patterns`, can and should be placed within topical or domain-specific subfolders in directories like `Models/2. Knowledge/` (e.g., `Models/2. Knowledge/Technical Analysis/`). This provides semantic grouping.
> 2.  **Functional Organization**: The `domain` field itself (and other metadata like `domain-category`) provides classification by the nature or role of the content.
>
> **Guideline**: While topical subfolders are essential for structural organization, AVOID creating subfolders *named identically* to `domain` field values (e.g., `Models/2. Knowledge/Concepts/` or `Projects/MyProject/Models/2. Knowledge/Patterns/`) if the `domain` frontmatter field is the primary or sole differentiator for the files intended for that folder. In such cases, the `domain` field in frontmatter fulfills this classification role, and the folder would be redundant. Rely on the `domain` field for this level of differentiation and use search/Dataview for aggregation.

## `status:` Values (Choose ONE)

- **`draft`**: Initial creation
- **`active`**: Currently being worked on
- **`in-progress`**: Ongoing development
- **`reviewed`**: Checked but not finalized
- **`finalized`**: Completed

## `tags:` Values (ONLY NOTE STATUS - NEVER SEMANTIC)

**ABSOLUTE RESTRICTION FOR `tags` FIELD:**
- The `tags` field is EXCLUSIVELY for note status.
- ONLY THE FOLLOWING THREE VALUES ARE EVER PERMITTED in the `tags` field:
    - **`notes-active`**: Currently being worked on (USE THIS 99% OF THE TIME)
    - **`notes-references`**: Verbatim sources
    - **`notes-research`**: Needs investigation
- **!!!ABSOLUTELY NO OTHER TAGS ARE ALLOWED!!!**
- **THIS MEANS NO**: methodology, content-processing, exercise, documentation, concepts, journal, implementation, code, analysis, project, task, or ANY OTHER descriptive/categorical tag.
- **UNDER NO CIRCUMSTANCES** use the `tags` field for content-based or thematic categorization. The `tags` field is STRICTLY for note status ONLY.
- If in doubt, use ONLY `notes-active`.

> **CRITICAL FORMATTING RULE**: If only one allowed tag applies, format as `tags: value`. If multiple allowed tags apply, use YAML list format with hyphens. THIS FORMAT IS MANDATORY AND MUST BE FOLLOWED WITH NO EXCEPTIONS.

## Special Fields (Use ONLY when appropriate)

- **`domain-category`**: ONLY for filter/group pages that collect or organize other notes
- **`source`**: ONLY when content comes from an external source