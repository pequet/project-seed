---
description: "Establishes standards for script headers, attribution, and branding for shell scripts."
globs: ["*.sh", "**/*.sh"]
alwaysApply: false
---
# Shell Script Attribution & Branding

**Ensure consistent and professional attribution, documentation, and branding for all shell scripts.**

When creating or modifying shell scripts in this project:

1.  **Analyze Script Context:** Determine purpose, execution method (interactive, automated), and project importance.
2.  **Select Appropriate Tier:**
    *   **Tier 1 (Interactive/Banner):** For interactively run scripts desiring prominent terminal branding.
    *   **Tier 2 (Standard Attributed):** For core project utilities or public-facing tools needing comprehensive source code header documentation.
    *   **Tier 3 (Minimal Utility):** For small helpers, simple wrappers, or internal utilities where a concise reference to the main project is sufficient.
3.  **Apply Chosen Template:** Use the appropriate template from the templates below. Populate all bracketed placeholders (e.g., `[YYYY-MM-DD]`, `[Detailed description...]`) with script-specific information for this project.

## Script Templates

### Tier 1 Template: Interactive/Banner Script
```bash
#!/bin/bash

# Standard Error Handling
set -e
set -u
set -o pipefail

# ASCII Art Banner
echo "
█ █ █  Project Name
 █ █   Version:  1.0.0
 █ █   Author:   Your Name
█ █ █  Github:   https://github.com/user/repo/
"

# Purpose:
#   [Detailed description of the script's purpose...]
#
# Usage:
#   ./your_script_name.sh [options] [arguments]

```

### Tier 2 Template: Standard Attributed Script
```bash
#!/bin/bash

# Standard Error Handling
set -e
set -u
set -o pipefail

# █ █ █  Project Name: Sub-System
#  █ █   Version: 1.0.0
#  █ █   Author: Your Name
# █ █ █  GitHub: https://github.com/user/repo/
#
# Purpose:
#   [Detailed description of the script's purpose...]
#
# Usage:
#   ./your_script_name.sh [options] [arguments]

```

### Tier 3 Template: Minimal Utility Script
```bash
#!/bin/bash

# Standard Error Handling
set -e
set -u
set -o pipefail

# Author: Your Name
# Purpose: [Brief one-line description...]
# Project: https://github.com/user/repo/

```