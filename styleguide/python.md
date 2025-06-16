<!--
SPDX-FileCopyrightText: © 2025 open-nudge <https://github.com/open-nudge>
SPDX-FileContributor: szymonmaszke <github@maszke.co>

SPDX-License-Identifier: Apache-2.0
-->

# Python styleguide

> ![CAUTION]
> Rules exist, but so do exceptions. Always evaluate each case individually.

## Table of contents

- [Base guidelines](#base-guidelines)
- [PEP8](#pep8)
- [Google style guide](#google-style-guide)
    - [Linting](#linting)
    - [Imports](#imports)
    - [Packages](#packages)
    - [Exceptions](#exceptions)
    - [Nested classes and functions](#nested-classes-and-functions)
    - [Comprehensions and generators](#comprehensions-and-generators)
    - [Generators](#generators)
    - [Lambda functions](#lambda-functions)
    - [Properties](#properties)
    - [True/False evaluations](#truefalse-evaluations)
    - [Lexical scoping](#lexical-scoping)
    - [Decorators and context managers](#decorators-and-context-managers)
    - [Class and Static Methods](#class-and-static-methods)
    - [Power Features](#power-features)
    - [Type Annotations](#type-annotations)
    - [Inheritance](#inheritance)
    - [Miscellaneous](#miscellaneous)

## Base guidelines

Refer to these guides first:

- [General](./README.md)
- [PEP8](https://peps.python.org/pep-0008/)
- [Google](https://google.github.io/styleguide/pyguide.html)

## PEP8

PEP8 is our default style guide. Minor deviations are allowed,
but significant departures should be considered errors.

> ![CAUTION]
> Skim through PEP8 before proceeding.

## Google style guide

Most principles apply, with these modifications:

### Linting

> ![NOTE]
> Linting is automated via [opentemplate](https://github.com/open-nudge/opentemplate).

The goal is to improve linting coverage in order to automate
as many styleguide rules as possible.

### Imports

> ![NOTE]
> Prefer `import X` over `from X import Y`.

__Reasons:__

- Clarifies dependencies at the top of the file.
- Avoids namespace pollution.

Use `import X as Y` only for well-known aliases (e.g., `import pandas as pd`).

### Packages

> ![NOTE]
> Use `from <PATH> import <MODULE>` only for internal modules.

__Pros:__

- Clear module hierarchy.
- Differentiates internal vs. third-party dependencies.
- Submodules can be moved/renamed more intuitively.

### Exceptions

- Define custom exceptions if they improve clarity.
- Avoid catch-all exceptions unless absolutely necessary.
- Prefer [contextlib](https://docs.python.org/3/library/contextlib.html) over `finally`.

### Nested classes and functions

> ![NOTE]
> Avoid nested classes and functions.

Instead, use:

- Helper functions/methods.
- Separate modules.

__Reasons:__

- Nested structures hinder testing and readability.
- Encourages modular design.

### Comprehensions and generators

> ![NOTE]
> Limit nesting to one level and basic functions.

Allowed:

```python
result = [transform(x) for x in iterable if predicate(x)]
```

`transform` and `predicate` might be more complex functions.

### Generators

> ![NOTE]
> Prefer generators over lists whenever possible.

__Pros:__

- More memory-efficient.
- Convertible to a list if needed (`list(generator(...))`) by one-liner.

### Lambda functions

> ![NOTE]
> Use only for basic expressions (≤40 characters).

Prefer [operator module](https://docs.python.org/3/library/operator.html) when applicable.

### Properties

> ![NOTE]
> Avoid setters and getters; use native properties when possible.

Instead:

- Pass required attributes in `__init__`.
- Redesign code to minimize state changes.

### True/False evaluations

> ![NOTE]
> Prefer `None` over empty lists/tuples/dicts.

__Pros:__

- `None` signals missing data more explicitly.
- Improves typing clarity.

### Lexical scoping

> ![NOTE]
> Avoid lexical scoping.

Sometimes they are necessary, but you should probably pass them to the
function directly.

### Decorators and context managers

> ![NOTE]
> Encouraged but must be well-implemented.

__Common use cases:__

- Logging.
- Performance measurement.
- Resource management (e.g., database connections).

__Remember:__

- Prefer context managers over `finally`.
- Always re-raise exceptions when wrapping functions.

### Class and Static Methods

> ![NOTE]
> Favor object encapsulation over class methods.

Class methods are useful for multiple constructors
(`from_csv`, `from_json`).

> ![CAUTION]
> Avoid static methods unless overriding is __definitely__
> never required.

### Power Features

> ![NOTE]
> Use metaclasses and attribute overrides (`__getattr__`, `__setattr__`)
> only if absolutely necessary.

Carefully weigh maintainability, complexity, and readability.

### Type Annotations

> ![NOTE]
> Annotate everything except `self` and `cls`.

__Best practices:__

- Use type aliases for deep nesting (`3`/`4` levels or more).
- Prefer `import typing` over `from typing import X`
    (see imports section for rationale).

Example:

```python
SpecialType = dict[str, list[str]]


def foo(x: list[SpecialType]) -> None: ...
```

### Inheritance

> __Limit inheritance depth to ~3 levels.__

- Abstract base classes are fine for defining interfaces.
- __Avoid multiple inheritance__ unless implementing mixins
    (decide on a case-by-case basis).

### Miscellaneous

- Use [opentemplate](https://github.com/open-nudge/opentemplate) for linting.
- Prefer `@property` over getters/setters.
- Write an entrypoint `main` function guarded by `if __name__ == '__main__'`.
