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
- [commition](#commition)
- [A](#a)
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

## commition

> ![CAUTION]
> We are here currently!

Immutable commit-only based versioning for Python projects helping with
[some behavioral pitfalls](https://hynek.me/articles/semver-will-not-save-you/) of
[semantic versioning](https://semver.org/) scheme.

> ![CAUTION]
> Click here to view the repository.

## A

Unified logging library for CLI and production application.

## B

Opinionated linter checking best Python practices

## C

Opinionated linter checking best documentation practices

## D

Opinionated linter checking best GitHub Actions practices

## E

Library to create checkers/linters

## F

Linter verifying opennudge coherence

## G

Opinionated linter checking best PyTorch practices

## H

Small PyTorch library for memory-efficient optimization in PyTorch

## I

Layers shape inference in PyTorch

## J

Improved PyTorch datasets experience

## K

Library providing a unified metadata of a given PyTorch
run (e.g. seed, sample order, configuration etc.)

## L

Raw data validation framework

## M

Reusable Python mixins for library creation

## N

Reusable Python structures for library creation

## O

Flexible and zero-abstraction prompt chaining library
(batteries included!)

## P

Most pleasant configuration library in Python

## Q

Adapter library converting objects and types of pydantic-like libraries
(e.g. [`sqlmodel`](https://github.com/fastapi/sqlmodel),
[`strawberry-graphql`](https://github.com/strawberry-graphql/strawberry),
[`polyfactory`](https://github.com/litestar-org/polyfactory)

## R

Attestation of `pytest` results (as described by
[this predicate](https://github.com/in-toto/attestation/blob/main/spec/predicates/test-result.md))

## S

`pydantic`-first data generation library similar to [`gentab`](https://github.com/omaralvarez/gentab)
targeting complex column inter-dependence generation asynchronously (depends on `O`)

## T

Small tool (integrated with, e.g. `pre-commit`) indicating whether the change
is breaking and is marked correctly as such in semantic versioning.

## U

Semantic harden-runner
(see [harden-runner](https://github.com/step-security/harden-runner)) which
allows to specify whole categories of enabled endpoints instead of
individual ones.

## V

OSV-Scanner management tool reading `pyproject.toml` and excluding
vulnerabilities (if dev dependencies only) automatically.

Exception management which automates it and allows for scripting.

## W

Pyproject.toml separator which allows to hook different systems
(e.g. `pre-commit`) on sub-file changes.
