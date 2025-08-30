---
type: capture
domain: inbox
subject: Seed Project
status: active
tags: notes-active
summary: "Plan to refactor the Seed project into a self-aware, publishable boilerplate repository with dedicated framework documentation."
---

# Plan: Create a Self-Aware Boilerplate Repository

## 1. Goal

Refactor the `Seed` project's structure to treat the public repository boilerplate as the primary published artifact. This boilerplate will be "self-aware," documenting its own context within the larger framework.

## 2. Rationale (Proof of Concept)

Publishing the boilerplate as a standalone repository serves as a proof of concept for the framework's submodule development strategy. It demonstrates how to maintain a public project's integrity while leveraging a private, version-controlled context for development artifacts (logs, notes, etc.).

## 3. Key Decisions & Structure

-   **Unit of Publication:** The folder `Projects/Seed/project-seed/Views/Public Repositories/Cursor Project Boilerplate/cursor-project-boilerplate/` will be renamed to something like `Cursor Project Boilerplate` and will be treated as the root of the public Git repository. The parent `Public Repositories` folder will *not* be published.
-   **Self-Aware Documentation (The "Mirror"):** The boilerplate will contain documentation that explains its relationship to the framework.
-   **Separation of Concerns:** This meta-documentation will reside in `docs/000-Framework-Context.md`, not the main `README.md`. The `README.md` will link to it.

## 4. Structure 

```text
Projects/
└── Seed/
    ├── Controllers/
    ├── Models/
    │   ├── 0. Inbox/
    │   ├── 1. Projects/
    │   ├── 2. Knowledge/
    │   ├── 3. Resources
    │   ├── 4. Archives/
    └── Views/
        └── Public Repositories/
            └── Public Repository Templates/               # This is the Grouping
                ├── cursor-project-boilerplate/            # This is the Public Repo Root
                │   ├── .gitignore
                │   ├── .cursor/
                │   ├── .repomixignore
                │   ├── .specstory -> ../private/.specstory
                │   ├── .vscode/
                │   ├── .repomixignore/
                │   ├── assets/                        
                │   ├── docs/
                │   │   └── 000-Framework-Context.md 
                │   ├── LICENSE
                │   ├── memory-bank/
                │   ├── README.md
                │   └── scripts/
                │   │   └── run_main_script.sh
                └── private/                               # Assets tracked by the parent framework
                    └── .specstory
```

## 5. Action Items

1.  DONE Renamed `cursor-project-boilerplate` to its final, chosen name (e.g., `cursor-project-boilerplate`).
2.  Create `docs/000-Framework-Context.md` inside the boilerplate.
3.  Write the content for the new context document, explaining the "mirror" concept and the workflows (Inbox, Archives, etc.).
4.  Update the boilerplate's main `README.md` to be simpler and link to the new context document.
5.  Update the `Creating New Project.md` guide to reflect this new, more nuanced procedure. 