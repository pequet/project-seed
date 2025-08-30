---
description: "COMMAND: Always use a system `date` command for any timestamping. NEVER use placeholders or manual entry."
globs: ["*", "**/*"]
alwaysApply: true
---
# Timestamp Accuracy Protocol

- **ALWAYS USE A SYSTEM COMMAND** to fetch the current date and time for all logs, filenames, and other timestamps.
- **NEVER** use placeholders (e.g., `[current_date]`) or manual entries.
- **FOR FILENAMES & LOGS:** Use `date +%Y-%m-%d_%H%M`.
- **FOR DAILY HEADERS:** Use `date +%Y-%m-%d`.