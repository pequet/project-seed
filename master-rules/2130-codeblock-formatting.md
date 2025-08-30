---
description: "COMMAND: Ensure copy-pastable code blocks have no leading indentation and are surrounded by blank lines for readability."
globs: ["*.md", "**/*.md"]
alwaysApply: false
---
# Codeblock Formatting Protocol

- **FOR COPY-PASTABLE CONTENT** (e.g., shell commands, config snippets), format code blocks as follows:
  1.  **NO LEADING INDENTATION:** The ` ``` ` fences and all lines of code within them **MUST** start at column 0.
  2.  **SURROUND WITH BLANK LINES:** **ALWAYS** place a blank line before the opening and after the closing.

- **THIS APPLIES EVEN IN LISTS:** If a code block is inside a list item, the code block itself must still start at column 0 and be surrounded by blank lines.