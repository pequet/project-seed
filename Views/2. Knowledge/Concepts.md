---
type: view
domain: concepts
subject: Seed Project
status: draft
tags: notes-active
summary: A view of concepts relevant to the Seed Project.
---

# Concepts View (Seed Project)

## Overview

This view presents concepts relevant to the Seed Project. It follows the principles outlined in the core framework's [[Core/Models/2. Knowledge/Concepts]] hub file.

> [!seealso]
> This view is related to the core concept hub: [[Core/Models/2. Knowledge/Concepts]].

## Seed Project Concepts

```dataviewjs
// This DataviewJS block displays all concepts in the Seed Project
// It demonstrates a proper metadata-based approach to finding concepts

const concepts = dv.pages()
    .where(p => 
        p.domain === "concepts" && 
        p.subject === "Seed Project" &&
        p.type !== "view" // Exclude view files
    );

if (concepts.length > 0) {
    // Group concepts by their domain-category
    const categorizedConcepts = {};
    
    concepts.forEach(p => {
        let category = "Uncategorized";
        
        if (p["domain-category"]) {
            if (Array.isArray(p["domain-category"])) {
                // Use the first category if there are multiple
                category = p["domain-category"][0];
            } else {
                category = p["domain-category"];
            }
        }
        
        // Initialize the category array if it doesn't exist
        if (!categorizedConcepts[category]) {
            categorizedConcepts[category] = [];
        }
        
        // Add the concept to its category
        categorizedConcepts[category].push(p);
    });
    
    // Display concepts by category
    for (const [category, conceptsList] of Object.entries(categorizedConcepts)) {
        // Format the category name for display
        const displayCategory = category
            .split('-')
            .map(word => word.charAt(0).toUpperCase() + word.slice(1))
            .join(' ');
        
        dv.header(3, displayCategory);
        
        dv.table(["Concept", "Description"],
            conceptsList.map(p => [
                dv.fileLink(p.file.path),
                p.summary || "No description available"
            ])
        );
    }
} else {
    dv.paragraph("No concepts found. As you add concepts to your Seed Project, they will appear here.");
}
``` 