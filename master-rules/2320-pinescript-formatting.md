---
description: "COMMAND: Enforce Pine Script v5 formatting standards, including camelCase naming, script organization, and explicit typing."
globs: ["*.pine", "**/*.pine"]
alwaysApply: false
---
# Pine Script v5 Formatting Standards

## Naming Conventions

- **`camelCase`** for all variables and functions (e.g., `maFast`, `roundedOHLC()`).
- **`SNAKE_CASE`** (all caps) for constants (e.g., `BULL_COLOR`, `MAX_LOOKBACK`).
- **SUFFIX** variable names with their type or purpose where it adds clarity (e.g., `maLengthInput`, `bearColorInput`).

## Script Organization

- **MAINTAIN** a consistent script structure:
  1.  `//@version=5`
  2.  Declaration (`indicator()`, `strategy()`, or `library()`)
  3.  Import statements
  4.  Constant declarations
  5.  Inputs
  6.  Function declarations
  7.  Calculations
  8.  Strategy calls
  9.  Visuals (plots, fills, etc.)
  10. Alerts

## Spacing & Formatting

- **SPACING:** Use a space on both sides of all operators (`=`, `+`, `?`, etc.).
- **LINE WRAPPING:** Use an indentation level that is not a multiple of four (e.g., two spaces) to wrap long lines for readability.
- **EXPLICIT TYPING:** Declare variable types explicitly for clarity (e.g., `float ma = ta.sma(close, 14)`).