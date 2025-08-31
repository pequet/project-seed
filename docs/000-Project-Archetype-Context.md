---
type: guide
domain: methods
subject: Seed Project
status: active
tags: notes-active
summary: "Explains the project's context within the parent framework."
---

# Project Archetype Context

## Framework Context

This project, while a self-contained unit of work, is designed to exist as a **Project-Level Archetype** within the larger TRI framework. This document serves as a "convex mirror," looking out from the Project to show its place within the larger system, embodying the design principle: "when in doubt, zoom out."

### A Progressively Unfolding Structure

The parent framework's architecture is best understood by progressively unfolding its layers, from the highest level down to the specific location of this Project.

#### Level 1: The `Core` and `Projects`

At the highest level, the entire system is divided into two main parts:

```text
Root/
├── Core/         # The stable, shared foundation
└── Projects/     # Modular "plugins" that extend the Core
```

-   **`Core`:** Contains the stable, foundational elements of the system, including all Analytical Lenses.
-   **`Projects`:** A collection of modular "plugins" that extend the `Core`. This project is one such plugin.

#### Level 2: Locating the Project

Projects are the primary modular components of the framework, residing at the following path:

```text
Projects/
└── [Project Name]/      # This is the Project Archetype Boundary
```

While a Project has its own internal MVC structure, it operates as a distinct, outcome-focused module within the broader framework.

---

## The MVC Pattern in Projects

Each Project is organized using the Model-View-Controller (MVC) architectural pattern:

```text
Projects/
└── [Project Name]/
    ├── Controllers/  # Logic connecting Models and Views
    ├── Models/       # Data and business logic
    └── Views/        # User interfaces and public-facing elements
```

-   **Models**: Holds the project-specific data, knowledge, and concepts. This is the heart of your project's information.
-   **Views**: Contains all user-facing interfaces, dashboards, and visualizations of the data held in the Models.
-   **Controllers**: The operational logic, methods, and processes that act upon the Models and are surfaced in the Views.

## The Action-Oriented Structure for Models

The `Models` directory is further structured using an action-oriented (PARA-like) method to organize information based on its actionability:

```text
Models/
├── 0. Inbox/       # For capturing all new, unprocessed information
├── 1. Projects/    # Actionable sub-projects with defined goals
├── 2. Knowledge/   # Curated, long-term knowledge and insights
├── 3. References/  # Supporting materials and external resources
└── 4. Archives/    # Completed or inactive items
```

This structure ensures that all information has a logical place, whether it's a fleeting idea or a foundational piece of knowledge.

## Development Principles

This layered structure enables a powerful and organized development workflow guided by two key principles:

-   **Inbox-Driven Development:** All new ideas, notes, and tasks related to this project are first captured in `Models/0. Inbox/` before being processed into the appropriate location.
-   **Archival Over Deletion:** Following the framework's "never delete" principle, files are moved to `Models/4. Archives/` instead of being deleted, preserving a complete history of the project's evolution.