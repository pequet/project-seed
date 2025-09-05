---
type: hub
domain: system-state
subject: Seed Project
status: active
tags: notes-active
summary: "Hub page displaying the validation status of the 'domain' frontmatter field against the approved system."
domain-category: [knowledge-organization]
---

# Domain Validation 

This hub dynamically validates actual `domain` field usage across the Seed Project against the canonical list defined in [[Projects/Seed/knowledge-dictionary/domain-map]]. It provides real-time insight into which domain values are properly validated, which might need attention, and how frequently each value is used.

```dataviewjs
const { KnowledgeOrganizationManager } = customJS;
KnowledgeOrganizationManager.renderSimpleOrganizationTable(
    dv, 
    'domain', 
    dv.current().subject
);
```
