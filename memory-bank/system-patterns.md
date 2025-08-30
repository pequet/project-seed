---
type: overview
domain: system-state
subject: Project Seed
status: active
summary: High-level architecture, key design decisions, and system-wide patterns.
---
# System Patterns

## 1. System Architecture Overview

*   **Overall architecture & justification?** *(e.g., Monolithic, Microservices, Client-Server)*
    *   The project employs a **Core-Plugin Architecture** built upon a **Model-View-Controller (MVC)** pattern. This modular structure provides a stable, extensible foundation (Core) for project-specific implementations (Plugins). The justification is to separate the universal framework logic from the domain-specific application logic, enhancing maintainability, scalability, and reusability. The knowledge management aspect is organized using an **Action-Oriented Organization** principle, similar to PARA.

*   **High-Level Diagram Link (Recommended):**
    *   The architecture is described in detail in the root `ARCHITECTURE.md` file.

## 2. Key Architectural Decisions & Rationales

*   **Decision 1:** Implement the `memory-bank` as a core, nine-file system.
    *   **Rationale:** To create a standardized, comprehensive, and persistent context source for both human and AI collaborators. This ensures session continuity and reduces the cognitive load of onboarding or context-switching.

*   **Decision 2:** Use a `master-rules` directory to define AI agent behavior.
    *   **Rationale:** To enforce consistent, predictable, and high-quality interactions with AI assistants across different platforms, aligning their behavior with the project's core principles.

*   **Decision 3:** Structure the repository using an MVC-like pattern (`Models/`, `Views/`, `Controllers/`).
    *   **Rationale:** To enforce separation of concerns, making the system easier to navigate, understand, and extend. Models handle knowledge/state, Views handle presentation/interface, and Controllers handle methods/processes.

*   **Decision 4:** Adopt a "transparent documentation" approach to all documentation and context.
    *   **Rationale:** To make the project's evolution clear and lower the barrier for collaboration, whether the project is public or private.

## 3. Design Patterns in Use

*   **Core-Plugin Architecture:** The entire repository acts as a "core" framework that users will extend with their own "plugin" projects.
*   **Model-View-Controller (MVC):** The primary organizational pattern for the directory structure.
*   **Template Method Pattern:** The boilerplate itself is a template. The `memory-bank` files are sub-templates to be filled out, ensuring a consistent structure for every new project.
*   **Strategy Pattern:** The `master-rules` and AI-specific files (`CLAUDE.md`, `GEMINI.md`) allow for different AI "strategies" to be applied while maintaining a unified goal.

## 4. Component Relationships & Interactions

*   **AI Assistants <> `master-rules` & `memory-bank`:** AI assistants are instructed to treat the `memory-bank` as their primary source of truth for project context and to operate within the behavioral boundaries defined in `master-rules`.
*   **Developer <> `memory-bank`:** The developer's primary responsibility is to keep the `memory-bank` files (`active-context.md`, `development-log.md`, etc.) current, which in turn "teaches" the AI.
*   **Core Framework <> Project Implementation:** The boilerplate (Core) provides the structure and methodology. The user's specific code and documentation (Project) live within and extend this structure.

## 5. Data Management & Storage

*   **Primary Datastore & Rationale:**
    *   The filesystem is the primary datastore, utilizing structured Markdown files with YAML frontmatter.
    *   **Rationale:** This approach is simple, highly portable, version-controllable with Git, and both human- and machine-readable. It avoids vendor lock-in and complex database dependencies.

*   **Data Schema Overview/Link:**
    *   The implicit schema is defined by the YAML frontmatter keys within the Markdown files (e.g., `type`, `domain`, `subject`, `status`, `summary`).

## 6. Integration Points with External Systems

*   **System 1: AI Provider APIs (OpenAI, Google, Anthropic, etc.)**
    *   The boilerplate is designed to facilitate interactions with various AI models via integrated IDEs and tools.
*   **System 2: GitHub**
    *   The framework is designed for version control, collaboration, and public hosting on GitHub.
*   **System 3: Cursor IDE**
    *   Provides the tightest integration, with the `.cursor/rules` directory allowing for direct instruction of the IDE's AI capabilities.

---
**How to Use This File Effectively:**
This document outlines the technical blueprint of the system. Refer to it for understanding architectural choices, design patterns, and how components interact. Update it when significant architectural decisions are made, new patterns are introduced, or data management strategies change. It is crucial for onboarding new developers and ensuring consistent technical approaches.
