---
type: capture
domain: inbox
subject: Seed Project
status: new
tags: notes-active
summary: "Plan to document the 'Distraction-Free' or 'Dual-Context' development workflow for the boilerplate."
---

# Plan: Document the Dual-Context Workflow

## 1. Goal

Create a new document to explain the *procedural* "why" behind the boilerplate's structure. This document will focus on the benefits of the "Distraction-Free Mode" and the workflow of switching between the focused public repo context and the full framework context.

## 2. Rationale

The current `000-TRI-Framework-Context.md` explains the architectural context (looking "out"). This new document will explain the development *workflow* and its ergonomic benefits (looking "in" and switching). This is a crucial piece of documentation for any developer using the framework effectively.

## 3. Core Concepts to Document

-   **The "Distraction-Free" IDE Context:** Explain that the primary workflow is to open the public repo folder directly in an IDE to focus the context, reduce noise, and optimize tooling.
-   **Seamless Context Switching:** Emphasize the ability to switch between the focused repo view and the full `Seed` project view to access the parent `Models` (Inbox, Archives).
-   **Benefits of this Approach:**
    -   Reduces developer cognitive load.
    -   Improves performance and accuracy of AI tools, search, and linters.
    -   Enforces clean modularity and decoupling.
    -   Simplifies onboarding for collaborators.
    -   Maintains contextual integrity via symlinked private assets.
    -   Creates a clear "deployment" boundary.

## 4. Action Items

1.  Create a new document: `Projects/Seed/project-seed/Views/Public Repositories/seed-project-repo-name/docs/010-Development-Workflow.md`.
2.  Write the content for this new document, detailing the concepts and benefits listed above.
3.  Add a link to this new workflow document from the main `README.md` and/or the `000-TRI-Framework-Context.md` to ensure it's discoverable. 