---
type: view
domain: methods
domain-category: inbox-management
subject: Seed Project
status: draft
tags: notes-active
summary: Adaptive view of inbox items with priority-based organization and action tracking
---

```dataviewjs
// This is a reusable inbox view that works for both core and project inboxes.
// Just paste this code block in any inbox view - it automatically filters for the current page's subject.
//
// For items to appear in this view, they need these frontmatter fields:
// - domain: "inbox"
// - type: "capture"
// - subject: matches the current view's subject
// - priority: 1-4 (optional, defaults to 4)
// - status: for tracking item state
// - domain-category: for categorization (raw-transcript items are filtered out)

const { ConceptsManager } = customJS;
ConceptsManager.renderInboxView({ dv });
``` 