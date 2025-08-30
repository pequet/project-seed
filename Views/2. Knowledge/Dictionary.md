---
type: view
domain: concepts
subject: Seed Project
status: draft
tags: notes-active
summary: A view of the Seed Project's dictionary, providing a dynamic directory of its knowledge elements.
---

# Dictionary View (Seed Project)

## Overview

This view presents the Seed Project's dictionary, a dynamic directory of its knowledge elements. It follows the principles outlined in the core framework's [[Core/Models/2. Knowledge/Dictionary]] concept file.

> [!seealso]
> This view is related to the core concept: [[Core/Models/2. Knowledge/Dictionary]].

```dataviewjs
const { ConceptsManager } = customJS;
ConceptsManager.generateDictionaryView({ dv, startLevel: 2 });
``` 