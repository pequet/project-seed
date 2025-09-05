---
type: hub
domain: system-state
subject: Seed Project
status: active
tags: notes-active
domain-category: [knowledge-organization]
summary: "Simple alphabetical table view of domain categories with validation status and usage counts."
---

# Functional Validation 

This hub dynamically validates actual `domain-category` field usage across the Seed Project against the canonical list defined in [[Projects/Seed/knowledge-dictionary/functional-map]]. It provides a clean alphabetical table view of all domain categories with their validation status and usage counts, highlighting which categories are properly validated and which might need attention.

```dataviewjs
const { KnowledgeOrganizationManager } = customJS;
KnowledgeOrganizationManager.renderSimpleOrganizationTable(
    dv, 
    'domain-category', 
    dv.current().subject
);
```

