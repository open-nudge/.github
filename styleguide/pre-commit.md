<!--
SPDX-FileCopyrightText: © 2025 open-nudge <https://github.com/open-nudge>
SPDX-FileContributor: szymonmaszke <github@maszke.co>

SPDX-License-Identifier: Apache-2.0
-->

# Pre-commit

> ![CAUTION]
> Rules exist, but so do exceptions. Always evaluate each case individually.

## Table of contents

- [Linters](#linters)
- [Naming](#naming)
    - [Differentiate types](#differentiate-types)
- [IDs](#ids)
- [Version pinning](#version-pinning)
- [Order](#order)
- [Example](#example)

## Linters

Use checkers/linters to automatically verify your file, suggested ones:

- [adrienverge/yamllint](https://github.com/adrienverge/yamllint) - YAML style

> ![CAUTION]
> Automatic checks __may not be described__ in this document

## Naming

> ![NOTE]
> Use dash-case (hyphen, lower-case) __for every programmatic name__
> (e.g. `id` field value)

### Differentiate types

> ![NOTE]
> Hooks can be (approximately) divided into those modifying
> files and those which do not

Based on that differentiation you should prefix each hook's name
by `<<<FIX>>>` or `<<<CHECK>>>` (or other variations of this idea)
so the users can understand what happens after each
of those (for example applying changes again via `git add`).

## IDs

> ![NOTE]
> Each ID should be the same as the human-readable name of the hook
> without the prefix

For hooks performing fix and check afterwards __you can add the `fix`/`feat`__
prefix to differentiate different steps.

> ![CAUTION]
> You can use `alias` to rename hooks with predefined `id` fields.

## Version pinning

> ![NOTE]
> Each repository should be pinned to the commit, __not the version__

You can use the following command to update and freeze the dependencies:

```sh
pre-commit autoupdate --freeze
```

## Order

> ![CAUTION]
> Order of the hooks may change the outcome dramatically!

Hook ordering guidelines:

- Hooks possibly modifying the (approximately) largest
    number of files first
- Hooks modifying smaller parts of code
- Run non-modifying checks last

When it comes to user experience:

- Hooks rarely ran
- Hooks running fast
- Slower hooks

## Example

```yaml
repos:
  - repo: "https://github.com/google/osv-scanner/"
    # Pin by hash, not the version
    # frozen specifies the actual version
    rev: "0e986b49c4e7ee5aa545531c4a8908455f8a9e82"  # frozen: v2.0.0
    hooks:
      - id: "osv-scanner"
        name: "<<<CHECK>>> OSV Scanner"
        # Both hooks do the same, differentiate by prefix
  - repo: "https://github.com/this-does-not-exist/some-hook/"
    rev: "fegjkekfek7ee5aa545531c4a8908455f8a9e82"  # frozen: v2.71.3
    hooks:
      - id: "check-something"
        name: "<<<CHECK>>> Something"
      - id: "fix-something"
        name: "<<<FIX>>> Something"
```
