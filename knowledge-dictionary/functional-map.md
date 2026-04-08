---
type: overview
domain: system-state
subject: Seed Project
status: active
tags: notes-active
validates-field: domain-category
summary: "Master list of approved domain-category values for DataviewJS validation."
domain-category: [knowledge-organization]
---

# Master Domain Categories

This file defines the canonical list of approved `domain-category` values for use in frontmatter across the Seed Project. The `ConceptManager.js` script uses this file to validate the `domain-category` field in functional organization views. The system uses a strict `prefix-topic` convention to ensure vault-wide clarity and prevent naming collisions. Keep the `validates-field` frontmatter value in this note.

| Category                   | Definition                                       | Usage Context                                  |
| -------------------------- | ------------------------------------------------ | ---------------------------------------------- |

*This view is queried by DataviewJS to build validation arrays for the Functional Map.*