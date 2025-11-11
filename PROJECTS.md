<!--
SPDX-FileCopyrightText: © 2025 open-nudge <https://github.com/open-nudge>
SPDX-FileContributor: szymonmaszke <github@maszke.co>

SPDX-License-Identifier: Apache-2.0
-->

# Projects

This page outlines public projects, their brief descriptions, and
links to their respective repositories (if already released)

> ![NOTE]
> Unreleased projects are left unnamed due to
> [name squatting](https://en.wikipedia.org/wiki/Cybersquatting) concerns.

> ![CAUTION]
> Unreleased projects might be moved around and other projects
> may be added before them!

## Table of contents

- [.github](#github)
- [opentemplate](#opentemplate)
- [cogeol](#cogeol)
- [loadfig](#loadfig)
- [comver](#comver)
- [lintkit](#lintkit)
- [pynudger](#pynudger)
- [pratidoc](#pratidoc)
- [noqaexplain](#noqaexplain)
- [B](#b)
- [C](#c)
- [D](#d)
- [E](#e)
- [F](#f)
- [G](#g)
- [H](#h)
- [I](#i)
- [J](#j)
- [K](#k)
- [L](#l)
- [M](#m)
- [N](#n)
- [O](#o)
- [P](#p)
- [Q](#q)
- [R](#r)
- [S](#s)
- [T](#t)
- [U](#u)
- [V](#v)

## .github

Natural language documents about everything `opennudge` related like
projects, plans, styleguides and many more.

> ![CAUTION]
> Click [here](https://github.com/open-nudge/.github) to view the repository.

## opentemplate

Base template for every Python project at `opennudge`. Includes
checks, automation, security best practices, and more out of the box.

> ![CAUTION]
> Click [here](https://github.com/open-nudge/opentemplate) to view the repository.

## cogeol

Library to use with [cog](https://github.com/nedbat/cog) allowing users to
control what Python versions (e.g. always support three latest Python
versions and update them whenever necessary) their library use.

> ![CAUTION]
> Click [here](https://github.com/open-nudge/cogeol) to view the repository.

## loadfig

Library to load configuration from `pyproject.toml` or `.<TOOL-NAME>.yml` files
in a standardized way (including `git` repository finding
with no dependencies).

> ![CAUTION]
> Click [here](https://github.com/open-nudge/loadfig) to view the repository.

## comver

Immutable commit-only based versioning for Python projects helping with
[some behavioral pitfalls](https://hynek.me/articles/semver-will-not-save-you/) of
[semantic versioning](https://semver.org/) scheme.

> ![CAUTION]
> Click [here](https://github.com/open-nudge/comver) to view the repository.

## lintkit

Library to create checkers/linters in minutes.

> ![CAUTION]
> Click [here](https://github.com/open-nudge/lintkit) to view the repository.

## pynudger

Opinionated linter checking best Python practices

> ![CAUTION]
> Click [here](https://github.com/open-nudge/pynudger) to view the repository.

## pratidoc

Opinionated linter checking best documentation practices

> ![CAUTION]
> Click [here](https://github.com/open-nudge/pratidoc) to view the repository.

## noqaexplain

> ![CAUTION]
> We are here currently!

Linter checking explanation is provided for every noqa (or similar directive).

> ![CAUTION]
> Click [here](https://github.com/open-nudge/noqaexplain) to view
> the repository.

## B

Opinionated linter checking best GitHub Actions practices

## C

Linter verifying opennudge coherence

## D

Opinionated linter checking best PyTorch practices

## E

Unified logging library for CLI and production application.

## F

Small PyTorch library for memory-efficient optimization in PyTorch

## G

Layers shape inference in PyTorch

## H

Improved PyTorch datasets experience

## I

Library providing a unified metadata of a given PyTorch
run (e.g. seed, sample order, configuration etc.)

## J

Raw data validation framework

## K

Reusable Python mixins for library creation

## L

Reusable Python structures for library creation

## M

Flexible and zero-abstraction prompt chaining library
(batteries included!)

## N

Most pleasant configuration library in Python

## O

Adapter library converting objects and types of pydantic-like libraries
(e.g. [`sqlmodel`](https://github.com/fastapi/sqlmodel),
[`strawberry-graphql`](https://github.com/strawberry-graphql/strawberry),
[`polyfactory`](https://github.com/litestar-org/polyfactory)

## P

Attestation of `pytest` results (as described by
[this predicate](https://github.com/in-toto/attestation/blob/main/spec/predicates/test-result.md))

## Q

`pydantic`-first data generation library similar to [`gentab`](https://github.com/omaralvarez/gentab)
targeting complex column inter-dependence generation asynchronously (depends on `O`)

## R

Small tool (integrated with, e.g. `pre-commit`) indicating whether the change
is breaking and is marked correctly as such in semantic versioning.

## S

Semantic harden-runner
(see [harden-runner](https://github.com/step-security/harden-runner)) which
allows to specify whole categories of enabled endpoints instead of
individual ones.

## T

OSV-Scanner management tool reading `pyproject.toml` and excluding
vulnerabilities (if dev dependencies only) automatically.

Exception management which automates it and allows for scripting.

## U

Pyproject.toml separator which allows to hook different systems
(e.g. `pre-commit`) on sub-file changes.

## V

(Direct) dependency linter which checks if the included
dependencies are dependable and maintained.
(e.g. `pre-commit`) on sub-file changes.
