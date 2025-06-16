<!--
SPDX-FileCopyrightText: © 2025 open-nudge <https://github.com/open-nudge>
SPDX-FileContributor: szymonmaszke <github@maszke.co>

SPDX-License-Identifier: Apache-2.0
-->

# Styleguide

This guide outlines best practices for code structure across multiple
languages—unless a language-specific guide states otherwise.

> [!CAUTION]
> While rules exist, exceptions do too. Always consider each case individually.

## Table of Contents

- [Approach](#approach)
- [Linting](#linting)
- [Naming](#naming)
- [Modules](#modules)
- [Libraries](#libraries)
- [Language specific](#language-specific)

## Approach

To write high-quality code efficiently:

- __Break large projects into smaller ones__ – easier to manage, test, and refactor.

- __Refactor continuously__ – prevents unmanageable structures and saves time long-term.

- __Plan before and during coding__ – ask yourself:

    - What might change in the future?
    - How adaptable is my code to specification changes?
    - What would need updating for future extensions?

## Linting

Linters enforce many of these guidelines.
`opennudge` tries to maximize linter coverage to catch issues automatically.

> [!CAUTION]
> Prefer to turn off linter on a case-by-case basis instead of globally

## Naming

- Use __ONLY__ well-known abbreviations (e.g., `i` for index iteration).
- Keep names short—context should come from modules/namespaces.
- Use meaningful names; generic names are fine if they make sense.
- Prefer full module names for clarity, unless performance dictates otherwise.
- Ensure docstrings and code remain consistent.

## Modules

> [!CAUTION]
> "Modules" may refer to namespaces, packages, or projects,
> depending on the language.

- Group related functionality in a module to improve reusability and maintainability.
- If function/class names require multiple words, consider
    breaking them into separate modules.
- Repeating words across functions/classes often signals a need
    for a new module.
- __Avoid excessive nesting__ — deeply nested modules should be moved to
    separate packages/projects.
- Use `singular` names for modules unless a plural form makes more sense.

## Libraries

- Split reusable components into libraries (e.g., one for neural networks,
    another for data processing).
- __Prefer libraries over frameworks__ — libraries provide flexibility,
    while frameworks impose patterns.

## Language specific

- [Natural language](natural-language.md)
- [Python](python.md)
- [GitHub Actions](github-actions.md)
- [Pre-commit](pre-commit.md)
