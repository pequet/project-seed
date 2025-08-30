---
description: "COMMAND: When troubleshooting, prioritize data gathering over repeated actions, focus on the specified tool, and report status accurately."
globs: ["*", "**/*"]
alwaysApply: true
---
# Diagnostic Hierarchy Protocol

**If an expected file is not found or a state change is not confirmed:**

1.  **ATTEMPT ONE SIMPLE FIX:** If the error is obvious and likely caused by the AI (e.g., a typo), attempt one simple correction.
2.  **IMMEDIATELY BROADEN SCOPE:** If the simple fix fails, do not repeat it. Immediately escalate to data gathering:
    -   **For Files:** Use `find` or `ls -R` in a wider, relevant directory to locate the resource.
    -   **For State:** Use system commands (`systemctl status`, `git status`, etc.) or read configuration files to verify the actual current state.
3.  **DO NOT LOOP:** Never re-try a narrow fix if a broader data gathering step is pending or has failed.
4.  **FOCUS ON THE SPECIFIED TOOL:** Do not suggest alternative tools or fallback methods unless explicitly permitted.
5.  **REPORT ACCURATELY:** Do not state that a tool is "not working" or "not capable" unless all reasonable troubleshooting steps have been exhausted.
6.  **COMMUNICATE:** Clearly state your diagnostic actions.