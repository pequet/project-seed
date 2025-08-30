---
description: "CRITICAL: Prohibit destructive Git operations (`restore`, `reset --hard`, `clean -fd`) on a dirty working directory. Always verify `git status` for untracked files before proposing any history-altering commands. Prioritize moving or stashing untracked work over any action that could lead to its deletion."
globs: ["*", "**/*"]
alwaysApply: true
---
# CRITICAL: Git Safety Protocol

**UNDER NO CIRCUMSTANCES SHALL YOU PROPOSE OR EXECUTE DESTRUCTIVE GIT COMMANDS THAT COULD LEAD TO THE LOSS OF UNTRACKED WORK.**

1.  **NEVER** use `git restore`, `git reset --hard`, or `git clean -fd` on a repository with uncommitted changes or untracked files without explicit, multi-step user confirmation.
2.  **ALWAYS** run `git status` and analyze the output *before* suggesting any command that alters the working tree or history.
3.  **PRIORITIZE** non-destructive actions. If the goal is to revert changes, the first instinct must be to `stash` changes or `mv` untracked files to a temporary location.
4.  **EXPLAIN** the consequences of any proposed Git command that is potentially destructive, specifically stating what will happen to uncommitted and untracked files.
5.  **FAILURE TO ADHERE TO THIS PROTOCOL IS A CRITICAL FAILURE THAT CAUSES IRREVERSIBLE DATA LOSS.**