---
description: "Enforce strict frontmatter schema for all documents."
globs: ["*.md", "**/*.md"]
alwaysApply: true
---
# Frontmatter Standards

This file defines the complete frontmatter schema. All fields and values MUST conform to this specification.

| Field | Purpose & Allowed Values | Example |
| :--- | :--- | :--- |
| `type` | **(CHOOSE ONE)** Defines the note's function. Must not match `domain`. `overview`: Standard content note. `hub`: Navigation page. `guide`: How-to instructions. `procedure`: Formal step-by-step process. `log`: Chronological record. | `type: overview` |
| `domain` | **(CHOOSE ONE)** Defines the note's knowledge area. Must not match `type`. `concepts`: Foundational ideas. `patterns`: Recurring solutions. `methods`: Processes and workflows. `system-state`: System documentation. | `domain: concepts` |
| `status` | **(CHOOSE ONE)** The current state of the document. `draft`: Initial creation. `active`: In progress. `finalized`: Complete. | `status: draft` |
| `subject` | The broad context of the note. `General`: For Core/system-level notes. `[Project Name]`: For notes within a specific project. `[Lens Name]`: For notes within an analytical lens. | `subject: General` |
| `summary` | A brief, one-sentence description of the note's content. | `summary: "A concise explanation of [topic]."` |
| `tags` | **(CRITICAL)** For note status ONLY. No other tags allowed. `notes-active`: (Default) Being worked on. `notes-references`: Verbatim source. `notes-research`: Needs investigation. | `tags: notes-active` |
| `domain-category`| **(Optional)** For filter/group pages that collect other notes. | `domain-category: project-idea` |
| `source` | **(Optional)** The external origin of the content, if any. | `source: "https://example.com"` |

**Prohibited Fields:** `title`, `category`. Use the filename for the title.