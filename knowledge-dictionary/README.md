# Knowledge Dictionary

This directory serves three purposes for this context boundary:

1. **Vocabulary** — canonical definitions of key terms and concepts (`glossary.md`)
2. **Frontmatter validation** — approved values for metadata fields like `type`, `domain`, and `domain-category` (the map files)
3. **Structural organization** — the intended folder hierarchy for knowledge files (`structural-map.md`)

## Canonical Structure (5 files)

- **glossary.md** — Curated definitions of key terms, concepts, and patterns.
- **structural-map.md** — Defines the semantic folder hierarchy for knowledge files.
- **functional-map.md** — Maps approved `domain-category` values.
- **domain-map.md** — Maps approved `domain` values.
- **type-map.md** — Maps approved `type` values.

Each file uses a `validates-field:` key in its frontmatter to declare which frontmatter field it governs. Approved values are defined as rows in a Markdown table (first column = value, second = definition, third = usage context).

Boundary-level values are checked first. If a value isn't found locally, the root-level knowledge-dictionary is used as fallback.

## Validation

These files can be consumed by any tool that needs to validate frontmatter. Current implementations include:

- Obsidian DataviewJS validation hubs at `Core/Views/2. Knowledge/Knowledge Organization/Functional/` (Domain Validation, Type Validation, Functional Validation, Subject Validation) — powered by `Core/Views/Public Repositories/Obsidian/Concept Manager/obsidian-concept-manager/scripts/KnowledgeOrganizationManager.js`
- CLI health check at `Core/Controllers/Methods/Operations/Scripts/Self-Knowledge/tri-system-health.sh`
