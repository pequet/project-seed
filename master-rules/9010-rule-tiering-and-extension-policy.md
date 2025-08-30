---
description: "Defines the application of rule tiers (Universal, Standards, Context-Specific) at the Project level and outlines the policy for adding project-specific rules."
globs: ["master-rules/*.md", "**/master-rules/*"]
alwaysApply: false
---
# 9010: Rule Tiering and Extension Policy (Project Level)

## 1. Purpose

This document provides a definitive analysis of how the framework's rule tiers apply to a **Project Archetype**. It confirms that the current rule set is appropriate and establishes the formal policy for extending it with project-specific rules as the project evolves.

## 2. Rule Tier Application at the Project Level

The `Rules Distribution Matrix` specifies a tier requirement of **"U + S (progressive adoption)"** for the Project Archetype. This means the `Project Seed` must contain the full set of both tiers, which serves as a comprehensive starting point for any new project.

The evaluation of the current rules is as follows:

| Rule Series | Tier | Analysis at Project Level | Verdict |
| :--- | :--- | :--- | :--- |
| **0000-9000s** | **U** | The Universal series (0000, 1000s, 9000s) provides the non-negotiable baseline for safety, behavior, and integrity. These are **mandatory** for any project to ensure it operates safely within the framework. | **Correctly Placed** |
| **2000 Series** | **S** | The Standards series provides a complete library of best practices for architecture, content, workflows, and scripting. Their inclusion in the seed is correct, allowing a newly spawned project to **adopt the standards relevant to its specific domain** (e.g., a data science project might use PineScript rules, while a web app would not) and discard the rest. | **Correctly Placed** |
| **9999 Index** | **S** | The index is required at any level distributing Tier S rules. Its presence is mandatory for the Project Seed. | **Correctly Placed** |

### Conclusion
The Project Seed correctly contains the complete set of Universal and Standard rules. This provides maximum safety and a complete library of optional standards, fulfilling the "progressive adoption" strategy.

## 3. Policy for Level-Specific Rule Extension (Tier C)

As a project develops unique requirements, it may be necessary to add **Tier C (Context-Specific)** rules that apply only within that project's boundary.

### Guiding Principle
Tier C rules are for narrow, localized, or experimental augmentations. They **must not** duplicate or conflict with the logic in existing Tier U or S rules. Their purpose is to handle a project's unique needs without polluting the universal standard set.

### Numeric Range for Tier C Rules
-   **Reserved Range:** `3000-3999`
-   This range is exclusively for project-specific rules and will be ignored during framework-level synchronization.

### Procedure for Adding a Tier C Rule
1.  **Justify the Need:** Clearly define why the new rule is necessary and why its logic is not already covered by an existing Tier U or S rule.
2.  **Select a Number:** Choose an unused number within the `3000-3999` range.
3.  **Write the Rule:** Author the rule following the standards in `9000-effective-rule-writing.md`.
4.  **Add to Index:** Update the project's local `9999-index.md` to include the new Tier C rule.

### Example Tier C Rule Justification

-   **File:** `3010-trading-api-key-validation.md`
-   **Justification:** "This project interfaces with a specific financial data API that has a unique key format (`[PROD|TEST]-[A-Z]{4}-[0-9]{8}`). This rule enforces the validation of this specific format, a requirement that is too narrow for a universal (Tier U) or general standard (Tier S) rule."
