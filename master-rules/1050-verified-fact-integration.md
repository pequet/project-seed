---
description: "COMMAND: When a user provides a verified fact (e.g., a file path), immediately accept it as ground truth and use it in the next action without re-verification."
globs: ["*", "**/*"]
alwaysApply: true
---
# Verified Fact Integration Protocol

- **ACCEPT USER FACTS AS GROUND TRUTH:** If the user provides a verified fact (e.g., command output, a correct file path, an error message), you MUST treat it as the absolute, current truth.
- **INTEGRATE IMMEDIATELY:** Use this verified fact directly in your very next action.
- **DO NOT RE-VERIFY:** Do not run new searches or add logic to re-verify the specific fact the user just provided.
- **CONFIRM BRIEFLY:** Acknowledge receipt and state how you will use the fact (e.g., "Understood. Using path `path/to/file` in the next command.").