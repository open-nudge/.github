<!--
SPDX-FileCopyrightText: © 2025 open-nudge <https://github.com/open-nudge>
SPDX-FileContributor: szymonmaszke <github@maszke.co>

SPDX-License-Identifier: Apache-2.0
-->

# GitHub Actions

> [!CAUTION]
> Rules exist, but so do exceptions. Always evaluate each case individually.

## Table of contents

- [Linters](#linters)
- [Naming](#naming)
    - [Job casing](#job-casing)
    - [Workflow name](#workflow-name)
    - [Job name](#job-name)
        - [Example](#example)
    - [Single-job workflows](#single-job-workflows)
    - [Steps naming](#steps-naming)
    - [Example 1](#example-1)
- [Data types](#data-types)
    - [Strings](#strings)
- [Concurrency](#concurrency)
    - [Use github.workflow_ref instead of github.workflow](#use-githubworkflow_ref-instead-of-githubworkflow)
- [Permissions](#permissions)
    - [Top-level](#top-level)
    - [Job-level](#job-level)
    - [Example 2](#example-2)
- [Conditionals](#conditionals)
- [Run](#run)
- [Reusable workflows](#reusable-workflows)
    - [File naming](#file-naming)
- [Custom actions](#custom-actions)
    - [Third-party](#third-party)
    - [Same organization](#same-organization)
    - [actions/checkout](#actionscheckout)
        - [persist-credentials](#persist-credentials)
        - [sparse-checkout](#sparse-checkout)
        - [sparse-checkout-cone-mode](#sparse-checkout-cone-mode)
        - [fetch-depth](#fetch-depth)
- [Security](#security)
    - [Harden runner](#harden-runner)

## Linters

Use checkers/linters to automatically verify your file, suggested ones:

- [woodruffw/zizmor](https://github.com/woodruffw/zizmor) - mainly security
    checks
- [adrienverge/yamllint](https://github.com/adrienverge/yamllint) - YAML style

> [!CAUTION]
> Automatic checks __may not be described__ in this document

## Naming

> [!NOTE]
> Use dash-case (hyphen, lower-case) __for every programmatic name__
> (e.g. file name, `id` field, job identifier etc.)

### Job casing

> [!NOTE]
> __Always__ use "Upper Case Job Names" (each word capitalized)

### Workflow name

> [!NOTE]
> __Always__ specify the top-level workflow name,
> __usually the same as the name of the file__ (but in a human-readable manner)

### Job name

> [!NOTE]
> Specify explicitly `name` field and
> __name it in the same <job-id>__ (but in a human-readable manner)

#### Example 1

> [!CAUTION]
> This example incorporates other naming rules as well

```yaml
# File name: another-job.yml
# Omitted other fields for brevity

name: "Another Job" # Same as file name

jobs:
  initial-job: # Same as top-level name as there is a single job
    name: "Initial Job" # Same as initial-job, but human-readable
  second-job:
    name: "Second Job" # Same as second-job, but human-readable
```

### Single-job workflows

> [!NOTE]
> If there is a single job in the workflow file
> __name it in the same way as the workflow-wide `name` field__

### Steps naming

> [!NOTE]
> __Always__ use `name` field for each `step`.
> Capitalize only the first letter of the `name`

### Example 2

> [!CAUTION]
> This example incorporates other naming rules as well

```yaml
# File name: super-job.yml
# Omitted other fields for brevity

name: "Super job" # Same as file name

jobs:
  super-job: # Same as top-level name as there is a single job
    name: "Super Job" # Same as super-job, but human-readable
    steps:
      name: "Say hello to everyone"
      run: >
        echo "Hello everyone!"
```

## Data types

### Strings

> [!NOTE]
> __Always__ use double quotation marks for __every__ string
> field in YAML unless using `>`/`>-`/`|`/`|-` for multiline strings.

Allows avoidance of unintuitive parsing of the data like `yes`/`no`
as booleans in some YAML versions.

## Concurrency

> [!NOTE]
> Specify `concurrency` explicitly on a global or per-job level
> depending on the use case

__Exception__: when all of the jobs should run simultaneously,
__which is likely rarely a case__.

### Use github.workflow_ref instead of github.workflow

> [!NOTE]
> Use `${{ github.workflow_ref }}` instead of `${{ github.workflow }}`
> as it is `name` parameter independent

Avoids concurrency issues when two workflows have custom names and
they happen to be equal.

## Permissions

### Top-level

> [!NOTE]
> Specify top-level empty permissions (`permissions: {}`)

Minimizes the likelihood of excessive permissions given
to any job on a level below.

### Job-level

> [!NOTE]
> Specify minimal job-level permissions

### Example

```yaml

permissions: {} # yamllint disable-line rule:braces

jobs:
  job:
    name: "Job"
    permissions:
      contents: "read"
```

## Conditionals

> [!NOTE]
> Every `if` conditional should be a multliline string expression
> specified via `>` and should omit `${{ }}` blocks.

Easier to spot and read

## Run

> [!NOTE]
> Every `run` should be a multliline string expression
> specified via `>` (single command) or `|` (multiple commands)

Easier to spot and read

## Reusable workflows

> [!NOTE]
> Should be used as a refactoring tool and for security
> purposes (e.g. [SLSA Level 3](https://slsa.dev/) compatible workflows)

### File naming

> [!NOTE]
> Every reusable workflow should have a `-reusable` postfix

For example `check-security-reusable.yml`

## Custom actions

### Third-party

> [!CAUTION]
> __Do not use custom third-party actions__ (unless they are ocming
> from trusted source)

Try to implement the functionality using `bash` and provided tooling
in GitHub runners (like [GitHub CLI](https://cli.github.com/)).

Such approach:

- minimizes potential attack surface
- easier to transfer to different CI systems
- (usually) easier to comprehend and adjust

### Same organization

> [!NOTE]
> Use them as a refactoring tool and to share common functionality

### [actions/checkout](https://github.com/actions/checkout)

#### persist-credentials

> [!NOTE]
> Set to `false` unless you want to `push` something to the repository

Does not leave the unnecessary credentials to be used by some `run`
or custom action

#### sparse-checkout

> [!NOTE]
> Specify data you want to checkout instead of checking out the full repository

- Allows the repository to grow with similar checkout time
- Action/run does not have to work with all the files

> [!CAUTION]
> Especially important for large `git` repositories

#### sparse-checkout-cone-mode

> [!NOTE]
> If possible, leave `sparse-checkout-cone-mode` to `true`

This sparse checkout focuses on __folders__ instead of files,
but should be significantly faster, especially if there are many patterns
to specify in `sparse-checkout`.

> [!CAUTION]
> It is also scheduled for depreciation due to performance issues

#### fetch-depth

> [!NOTE]
> Set to `1` (current default) unless the whole history is needed

## Security

### Harden runner

> [!NOTE]
> Use [step-security/harden-runner](https://github.com/step-security/harden-runner)
> __at the beginning of every job__

It allows to monitor and (most importantly) limit egress, which limits
the attack surface of nefarious actions and/or commits.
