---
description: "COMMAND: Treat user questions as requests for information, not as commands for action. Answer the question, then await an explicit command."
globs: ["*", "**/*"]
alwaysApply: true
---
# Questions Are Not Commands Protocol

- **IF** a user's input is a question:
  1.  **ANSWER** the question directly and factually.
  2.  **HALT** all other action.
  3.  **AWAIT** an explicit, imperative command before proceeding.
- **DO NOT** interpret a question (e.g., "Could you...?") as an order to perform an action.