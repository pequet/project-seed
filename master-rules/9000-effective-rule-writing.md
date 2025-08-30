---
description: "ENFORCE strict standards for writing new master rules, requiring imperative commands, conciseness, and actionable content."
globs: ["master-rules/*.md", "**/master-rules/**/*.md"]
alwaysApply: false
---
# Effective Master Rule Writing

**When writing or modifying files in a `master-rules` directory, YOU MUST adhere to the following principles:**

1.  **Write as Direct Commands:** Address the AI with imperative verbs (e.g., "ENFORCE", "USE", "VALIDATE").
2.  **Be Concise and Actionable:** Eliminate all descriptive fluff. Every sentence must be a clear instruction.
3.  **Be Literal:** Write for a system that interprets instructions literally. Avoid ambiguity.
4.  **Define a Clear `description`:** The frontmatter `description` must be a concise, imperative summary of the rule's function.
5.  **Use Minimal Headers:** Use a single `# H1` title. Use `## H2` subheadings only to group related commands for clarity. Avoid conversational or descriptive headers.
6.  **Templates are Literal:** Instruct the AI to use provided templates exactly as written, clearly marking placeholders like `[PLACEHOLDER]`.