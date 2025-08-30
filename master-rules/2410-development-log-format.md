---
description: "ENFORCE the correct format and procedure for updating Development Log files, ensuring reverse chronological order and comprehensive entries."
globs: ["**/development-log.md"]
alwaysApply: false
---
# Development Log Directives

**Reference:** `Core/Controllers/Methods/Guides/Memory Management/Procedures/Updating Memory Bank Files.md`

## Entry Format

- **ADD** new entries in reverse chronological order (newest at the top).
- **USE** the exact format: `## [[YYYY-MM-DD]]` for date headings.
- **DOCUMENT** the rationale for every change using bullet points under the date heading.
- **REFERENCE** all relevant file paths.
- **TAG** each entry with one of the following, using brackets: `[ARCHITECTURE]`, `[METHODOLOGY]`, `[DOCUMENTATION]`.

## Procedure for Significant Changes

- **FOLLOW** the update triggers defined in the `Memory Management` guide.
- **CROSS-REFERENCE** all log entries with the corresponding `Development Status` file to ensure consistency.