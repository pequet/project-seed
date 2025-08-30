---
description: "ENFORCE DataviewJS query standards, including metadata-based queries, path handling, and the canonical implementation pattern."
globs: ["*", "**/*"]
alwaysApply: true
---
# Dataview JS query standards

ALWAYS follow the guidelines in:

- [Dataview Patterns.md](mdc:Core/Controllers/Methods/Guides/Dataview Patterns.md) 

ALWAYS:

1. **Path Handling**
   - Use type:welcome page as root reference for the whole framework implementation
   - Use type:config page as root reference for the Core or the Project 
   - Strip root paths in displays
   - Never query by file paths

2. **Query Structure**
   - Filter using frontmatter metadata
   - Match current page subject
   - Validate property existence
   - Return plain objects

3. **Function Design**
   - Write reusable, parameterized functions
   - Default to current page context
   - Follow example patterns from guide

**Canonical Implementation Pattern**:

Start with the comments block explaining what the code does for the human who views the node source. and then for our friendly AI agents.

```dataviewjs
// This DataviewJS block implements a reusable query pattern for retrieving and displaying
// typed pages that share the same subject and domain categories as the current page.
// It follows core framework patterns by:
// 1. Using the welcome page to establish the framework root
// 2. Implementing type-based filtering with subject matching
// 3. Returning clean objects with path, status, and summary
// 4. Stripping root paths for display
//
// For our friends the AI Agents:
// This code simply finds and displays pages where:
// - type = "procedure"
// - domain-category matches current page
// - subject matches current page
// The output is a list of links to these pages with their summaries.

// Rule: Get framework root from welcome page
const welcomePage = dv.pages()
    .where(p => 
        p.type === "welcome" && 
        p.subject === "General"
    )
    .first();

// Rule: Use functions with parameters for reusable queries
const getPagesByType = (desiredType, subject = dv.current().subject) => {
    // Rule: Do not use file paths for queries, use frontmatter metadata
    return dv.pages()
        // Rule: Check if properties exist before using
        .where(p => p.type === desiredType && 
                   p["domain-category"] && 
                   p["domain-category"].includes(currentPage["domain-category"]) &&
                   // Rule: Match current page's subject
                   p.subject === subject)
        // Rule: Return plain objects, not dv objects
        .map(p => ({
            path: p.file.path,
            status: p.status,
            summary: p.summary
        }));
}

// Usage example showing clean array handling
const procedures = getPagesByType("procedure");
if (welcomePage) {
    const basePath = welcomePage.file.path.split('/').slice(0, -1).join('/');
    dv.list(procedures.map(p => 
        // Rule: Strip root path when displaying
        `[[${p.path.replace(basePath + "/", "")}]: ${p.summary}`
    ));
} else {
    dv.paragraph("No framework root found.");
}
```