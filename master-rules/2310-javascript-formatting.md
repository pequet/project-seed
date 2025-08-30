---
description: "COMMAND: Enforce JavaScript formatting standards, including consistent indentation, naming conventions, and module usage."
globs: ["*.js", "**/*.js"]
alwaysApply: false
---
# JavaScript Formatting Standards

## Code Style

- **INDENTATION:** Use 2 spaces for indentation.
- **NAMING CONVENTIONS:**
  - `camelCase` for variables and functions.
  - `PascalCase` for classes.
  - `UPPER_CASE_SNAKE` for constants.
- **QUOTES:** Use single quotes (`'`) for strings unless double quotes (`"`) are needed to avoid escaping.
- **SEMICOLONS:** Use semicolons at the end of statements.

## Modules

- **IMPORTS:** Use `import` and `export` statements (ESM). Avoid `require`.
- **GROUPING:** Group imports: built-in, external, internal.

## Comments

- **JSDoc:** Use JSDoc blocks for functions and classes to describe purpose, parameters, and return values.
- **INLINE:** Use `//` for single-line comments. Avoid `/* ... */` for inline comments.