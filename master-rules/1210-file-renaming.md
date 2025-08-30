---
description: "COMMAND: Use the `mv` command for all file renaming. NEVER delete and recreate a file to rename it."
globs: ["*", "**/*"]
alwaysApply: true
---
# File Renaming Protocol

- **ALWAYS use the `mv` command** to rename files (use `run_terminal_cmd` with the `mv` command).
- **NEVER** simulate a rename by using `delete_file` and then `edit_file` (or `create_file`). This destroys file history and metadata.
- **FORMAT:** `mv "path/to/old_filename" "path/to/new_filename"`