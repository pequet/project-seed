---
type: hub
domain: system-state
subject: Seed Project
status: active
tags: notes-active
summary: "Hub page displaying the validation status of the 'type' frontmatter field against the approved system."
domain-category: [knowledge-organization]
---

# Type Validation View

This hub dynamically validates actual `type` field usage across the Seed Project against the canonical list defined in [[Projects/Seed/knowledge-dictionary/type-map]]. It provides real-time insight into which type values are properly validated, which might need attention, and how frequently each value is used.

```dataviewjs
const { KnowledgeOrganizationManager } = customJS;
KnowledgeOrganizationManager.renderSimpleOrganizationTable(
    dv, 
    'type', 
    dv.current().subject
);
```
