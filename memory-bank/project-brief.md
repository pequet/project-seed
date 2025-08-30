---
type: overview
domain: system-state
subject: Project Seed
status: active
summary: Core project goals, requirements, and scope.
---
# Project Brief

## 1. Project Goal

*   **Primary Objective:** To create a well-structured, AI-ready boilerplate for new Projects, enabling faster, more transparent, and consistent development cycles, particularly within the Cursor IDE.

*   **Secondary Objectives (Optional):**
    *   To establish a clear methodology for human-AI collaboration on software Projects.
    *   To provide a "self-aware" repository structure where the Project's context and history are maintained within the repo itself via the `memory-bank`.
    *   To demonstrate best practices for developing projects, where documentation and process are as important as the code.

## 2. Core Requirements & Functionality

*   **Requirement 1:** A pre-configured directory structure that separates concerns (Models, Views, Controllers) and provides a dedicated space for AI context (`memory-bank`).

*   **Requirement 2:** Integrated and pre-configured rules and instructions for multiple AI assistants (Cursor, GitHub Copilot, Claude, Gemini) to ensure consistent behavior.

*   **Requirement 3:** A comprehensive `memory-bank` system to maintain Project state, goals, and technical context, enabling seamless session handoffs between human and AI collaborators.

*   **Requirement 4:** Clear documentation on the development workflow, architectural patterns, and AI collaboration protocols.

*   **Requirement 5:** A set of master rules that govern AI agent behavior, ensuring adherence to the Project's principles of clarity, efficiency, and accountability.

## 3. Target Audience

*   The primary target audience is software developers and teams using AI code assistants (especially Cursor) who are building Projects. This includes open-source maintainers, indie developers, and teams who want to standardize their AI-assisted development workflow and maintain high-quality, transparent documentation.

## 4. Scope (Inclusions & Exclusions)

### In Scope:

*   A complete, clonable repository structure with all necessary configuration files.
*   The nine-file `memory-bank` system with templates and usage instructions.
*   A `master-rules` directory with foundational rules for AI agent behavior.
*   Documentation for the architecture, workflow, and AI collaboration model.
*   Example configurations for different AI assistants (`CLAUDE.md`, `GEMINI.md`, `.cursor/rules`, etc.).

### Out of Scope:

*   Specific application logic or domain-specific code (it is a generic boilerplate).
*   Frontend frameworks, database integrations, or specific language dependencies beyond what's needed for the framework itself (Markdown, Bash, JSON).
*   Automated deployment scripts or CI/CD pipelines (though they can be added by the user).

## 5. Success Criteria & Key Performance Indicators (KPIs)

*   **Success Criteria:**
    *   **Clarity & Usability:** New users can understand the structure and start a Project with minimal friction.
    *   **AI Collaboration Efficiency:** The `memory-bank` and rules effectively provide context to AI agents, reducing repetitive explanations.
    *   **Adoption:** The boilerplate is used by others to start new Projects.

*   **Key Performance Indicators (KPIs):**
    *   Time from `git clone` to first meaningful Project-specific commit.
    *   Number of forks or Projects generated from this template on GitHub.
    *   Qualitative feedback from users on the clarity of the documentation and the utility of the `memory-bank`.

## 6. Assumptions

*   Users are familiar with Git, Markdown, and their chosen IDE (preferably Cursor).
*   Users have access to and have configured API keys for their chosen AI assistants.
*   Users are bought into the idea of maintaining structured documentation and context.

## 7. Constraints & Risks

*   **Constraints:**
    *   The framework's effectiveness is tied to the capabilities of the AI assistants it's designed to work with.
    *   The system relies on the user's discipline to keep the `memory-bank` updated.

*   **Risks:**
    *   **Stale Context:** The `memory-bank` becomes outdated, leading to incorrect guidance from AI agents. (Mitigation: Emphasize the `memory-bank` update process as a core part of the development workflow in the documentation).
    *   **Rapid AI Evolution:** The specific rules and configurations for AI agents may become outdated quickly. (Mitigation: Structure the rules modularly for easier updates and rely on high-level principles that are less likely to change).

## 8. Stakeholders

*   **Project Sponsor / Product Owner:** Benjamin Pequet
*   **Lead Developer:** Benjamin Pequet & AI Assistants
*   **Community:** Future users and contributors of the boilerplate.
    
## Template Usage Notes

This `project-brief.md` file, along with others in the `memory-bank/` directory, serves as a foundational part of the Memory Bank methodology. This system helps AI assistants maintain context and understanding across development sessions when working on a Project initiated from this template.

