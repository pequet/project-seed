---
type: hub
domain: system-state
subject: Seed Project
status: active
tags: notes-active
domain-category: [knowledge-organization]
summary: "Tree structure view of domain categories organized by namespace with dash-separated hierarchy."
---

# Functional Validation (Tree View)

This hub dynamically validates actual `domain-category` field usage across the Seed Project against the canonical list defined in [[Projects/Seed/knowledge-dictionary/functional-map]]. Unlike the standard tabular view, it displays domain categories in a hierarchical tree structure organized by namespace, making it easier to visualize the relationships between categories based on their dash-separated naming convention.

```dataviewjs
const { KnowledgeOrganizationManager } = customJS;
KnowledgeOrganizationManager.renderOrganizationTree({ 
  dv,
  debug: false
});
```

