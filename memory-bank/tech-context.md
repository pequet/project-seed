---
type: overview
domain: system-state
subject: Project Seed
status: active
summary: Technologies, setup, and technical constraints of the project.
---
# Technical Context

## 1. Technologies Used
*   **Knowledge Management:**
    *   Obsidian
    *   Markdown (with YAML frontmatter)
    *   DataviewJS
*   **AI Collaboration Stack:**
    *   Cursor IDE (primary)
    *   GitHub Copilot
    *   Claude Code
    *   Gemini CLI
    *   `vibe-tools` (for workflow automation)
*   **Core Technologies:**
    *   Git & GitHub
    *   Bash (for scripts)
    *   JSON (for configurations)

## 2. Development Setup & Environment
*   **Prerequisites:**
    *   An IDE that supports AI integration, preferably Cursor IDE.
    *   Git installed and configured.
    *   API keys for desired AI services (OpenAI, Google, etc.) configured for your tools.
    *   (Optional but Recommended) Obsidian for browsing the Markdown-based knowledge base and `memory-bank`.
*   **Setup Steps:**
    1.  Create a new repository from this template on GitHub or clone it directly.
    2.  Open the cloned repository in your IDE (e.g., Cursor).
    3.  Review the `memory-bank/` files, starting with `project-brief.md`, to customize the project context for your specific needs.
    4.  Follow the instructions in `README.md` to begin the development workflow.

## 3. Technical Constraints
*   **Tool Dependency:** The workflow is heavily optimized for the Cursor IDE. While usable in other editors, some of the deep integration and automated rule-following will be lost.
*   **Manual Upkeep:** The value of the `memory-bank` is directly proportional to the discipline of the developers in keeping it updated. It is not an automated system.
*   **AI Hallucination:** The system is designed to provide high-quality context to AI, but it does not eliminate the risk of AI making mistakes or "hallucinating" information. Developers must still verify AI-generated output.

## 4. Dependencies & Integrations (Technical Details)
*   **Cursor IDE:** The boilerplate includes a `.cursor/` directory with rules that directly instruct the IDE's AI features, enforcing specific behaviors and standards.
*   **GitHub:** The project is intended to be hosted on GitHub, leveraging its features for public repositories, collaboration (Pull Requests), and version control.
*   **Various AI APIs:** The effectiveness of the AI collaboration stack depends on access to external AI models through their respective APIs.

## 5. Code & Branching Strategy
*   **VCS:** Git
*   **Hosting:** GitHub
*   **Branching Model:** GitHub Flow is recommended. Create a new branch for each feature or significant change. `main` should always be in a deployable/usable state.
*   **Commit Messages:** Adherence to the Conventional Commits specification is strongly recommended to create an explicit and easily reviewable project history.

## 6. Build & Deployment Process
*   N/A - As a boilerplate, this project does not have a build or deployment process itself. The end-user's project, built from this template, will have its own specific build and deployment needs.

---
**How to Use This File Effectively:**
This document details the technical landscape of your project. Use it to understand the tools, setup procedures, constraints, and deployment workflows. Keep it updated as new technologies are adopted, setup steps change, or the deployment process evolves. It's essential for developer onboarding and maintaining a shared understanding of the tech stack.
