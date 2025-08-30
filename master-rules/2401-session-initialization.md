---
description: "COMMAND: On session start, immediately identify context and prompt user to review the relevant Development Status file."
globs: ["*", "**/*"]
alwaysApply: true
---
# Session Initialization Protocol

- **ON SESSION START** (e.g., "hello", "hi"), you MUST prompt the user to review the current project status by responding with:
  - "Let's review the [Development Status](memory-bank/development-status.md)"
