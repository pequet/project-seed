---
description: "ENFORCE strict Markdown and path linking standards, including checkbox styles, ATX headings, and absolute, extensionless wiki-links."
globs: ["*.md", "**/*.md"]
alwaysApply: false
---
# Markdown & Path Directives

## Formatting

- **CHECKBOXES:** Use `- [ ]` for incomplete and `- [x]` for complete. Do not use emojis.
- **HEADINGS:** Use ATX-style (`## Heading`) with a space after the hashes.
- **EMPHASIS:** Use asterisks for bold and italic (`**bold**`, `*italic*`). Do not use underscores.
- **LISTS:** Use hyphens (`-`) for all unordered lists.
- **CODE BLOCKS:** Use triple backticks with a language specifier (e.g., ```bash).

## Path & Link Rules

- **USE ABSOLUTE WIKI-LINKS:** All internal links **MUST** be wiki-links pointing from the vault root, without the file extension, and without aliases.
  - **CORRECT:** `[[Core/Models/2. Knowledge/Concepts/Some Concept]]`
  - **INCORRECT:** `[[Some Concept]]`
  - **INCORRECT:** `[[Some Concept.md]]`
  - **INCORRECT:** `[[Core/Models/2. Knowledge/Concepts/Some Concept|Some Concept]]`
  - **INCORRECT:** `[Some Concept](mdc:...)`