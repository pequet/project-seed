---
type: guide
domain: methods
subject: Seed Project
status: active
tags: notes-active
summary: "Explains the intended development workflow for a Project-Level Archetype."
---

# Project Development Workflow

This document outlines the intended workflow for developing a project within this archetype. The structure is designed to provide a clear path for information, from initial capture to final integration.

## The Core Workflow: From Inbox to Knowledge

The primary workflow follows a simple, powerful pattern:

1.  **Capture Everything in the Inbox:**
    -   Any new idea, task, piece of information, or raw note related to the project should be created as a new file in `Models/0. Inbox/`.
    -   This ensures that nothing is lost and that the rest of the project remains clean and organized.

2.  **Process the Inbox:**
    -   Regularly review the items in your Inbox.
    -   For each item, decide what it is and where it belongs.
        -   Is it a well-defined concept? Move it to `Models/2. Knowledge/`.
        -   Is it a task or a sub-project? Move it to `Models/1. Projects/`.
        -   Is it a supporting document? Move it to `Models/3. References/`.
        -   Is it no longer relevant but needs to be kept? Move it to `Models/4. Archives/`.

3.  **Build the Knowledge Base:**
    -   The core of your project lives in `Models/2. Knowledge/`. This is where you should formalize concepts, connect ideas, and build out your domain model using metadata-driven relationships.

4.  **Create Views and Dashboards:**
    -   Use the `Views/` directory to create dynamic, query-based visualizations of your knowledge.
    -   A dashboard in `Views/` might show all concepts with a certain tag, or all projects that are currently active.

5.  **Define Methods and Controllers:**
    -   Use the `Controllers/` directory to store reusable methods, scripts, or processes that act on your knowledge base.

## AI Collaboration

This workflow is designed for seamless human-AI collaboration:

-   **Use the Memory Bank:** Keep the `memory-bank/` directory updated, especially `active-context.md` and `development-log.md`. This is the primary way you provide context to your AI assistant.
-   **Leverage Master Rules:** The rules in `master-rules/` ensure the AI behaves consistently and follows the project's architectural principles.
-   **Generate Agent-Specific Docs:** Use the `ide-rules-synchronizer` script to generate documentation for your specific AI assistant from the `master-rules/`.

By following this workflow, you create a virtuous cycle: capturing raw information, processing it into structured knowledge, and then using that knowledge to build powerful views and methods, all while keeping your AI partner in sync.
