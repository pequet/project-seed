---
description: "COMMAND: Enforce standards for script formatting, attribution, terminal output, and section headers in all shell scripts."
globs: ["*.sh", "**/*.sh"]
alwaysApply: false
---
# Shell Script Standards

## Terminal Output Messages

1.  **SOURCE Utility Script:** Scripts REQUIRING formatted boxed messages MUST source `scripts/utils/messaging_utils.sh`.
2.  **USE `display_status_message` Function:** For script initiation, completion, failure, or key informational points.
3.  **USE Standard `status_char` Codes:** ` ` (Start), `x` (Success), `!` (Failure), `i` (Info), `?` (Prompt).

## Code Section Headers

1.  **USE Markdown-Style Hash-Asterisk Headers:**
    *   **Level 1 Header:** `# * Section Name`
    *   **Level 2 Header:** `# ** Sub-Section Name`
    *   **Level 3 Header:** `# *** Sub-Sub-Section Name`
2.  **ENSURE Space:** There MUST be a single space between the last asterisk and the `Section Name`.