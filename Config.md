---
type: config
domain: methods
status: active
subject: Seed Project
tags: notes-active
summary: Configuration settings for the Seed Project
valid_subjects: [Seed Project]
valid_filters: []
---

# Seed Project Configuration

This file provides configuration settings for the Seed Project, primarily for use with the DataviewJS components.

## Frontmatter Configuration

### Required Fields

- `type: config` - Identifies this as a configuration file
- `domain: methods` - Places this in the methods domain
- `subject: Seed Project` - Associates with the Seed Project
- `valid_subjects: [Seed Project]` - Defines valid subjects for this project
- `valid_filters: []` - Defines valid group types for relationship analysis (currently empty)

### Domain and Domain-Categories Usage

The frontmatter fields `domain` and `domain-category` serve specific purposes:

- **domain**: Identifies the type of content (e.g., concepts, patterns, groups)
  - Used in all files to specify their primary classification
  - Examples: `domain: concepts`, `domain: patterns`, `domain: groups`

- **domain-category**: Used ONLY in files that function as groups or hubs
  - Should NOT be added to regular concept or pattern files that aren't meant to function as groups
  - Specifies which group category the file belongs to
  - Examples: To be defined based on your project's needs

## DataviewJS Components

The Seed project uses several standard DataviewJS components:

- `ConceptsManager.generateViewTable`: Used in group hub files to display all concepts in that group
- `ConceptsManager.generateConceptsAnalysis`: Used in concept files to display all groups the concept belongs to
- `ConceptsManager.generateGroupItemsList`: Used in group pages to list all items belonging to that group
- `ConceptsManager.generateSmartView`: Smart component that combines the above functions based on the current page's metadata

### Smart View Component

The `generateSmartView` method is a powerful all-in-one component that automatically determines what to display based on the current page's metadata:

```
// This single block replaces the need for multiple separate blocks
const { ConceptsManager } = customJS;
ConceptsManager.generateSmartView({ 
    dv, 
    headerLevel: 2,
    groupItemsHeaderText: "Optional custom header for group items" 
});
```

## Usage Notes

### Adding a New Concept

1. Create a new file in the appropriate directory
2. Use frontmatter with `domain: concepts` 
3. Add group associations using the `group-[type]: [value]` pattern in frontmatter
4. Do NOT add `domain-category` unless the concept is also meant to function as a group
5. Include the `generateSmartView` component at the end of the file

### Adding a New Group

1. Create a new file in the appropriate Groups subdirectory
2. Use frontmatter with `domain: groups` and the appropriate `domain-category`
3. Include the `generateSmartView` component at the end of the file
