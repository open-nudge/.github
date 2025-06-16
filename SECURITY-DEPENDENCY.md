<!--
SPDX-FileCopyrightText: © 2025 open-nudge <https://github.com/open-nudge>
SPDX-FileContributor: szymonmaszke <github@maszke.co>

SPDX-License-Identifier: Apache-2.0
-->

# Environment dependencies policy

## Purpose

This policy describes how `.github` maintainers
consume third-party packages.

## Scope

This policy applies to all `.github` maintainers
and all third-party packages used in the `.github`
project.

## Policy

`.github` contributors __should not use any third-party packages__.

> [!CAUTION]
> This repository is `markdown`-cnetric and does not
> use any third-party packages.

> [!IMPORTANT]
> A few basic GitHub Actions are used to automate the
> security posture, adapted from
> [opennudge/opentemplate](https://github.com/open-nudge/opentemplate)

## Enforcement

This policy is enforced by the `.github` maintainers.
Maintainers are expected to review each other's code changes to ensure
that they comply with this policy.

## Exceptions

Exceptions to this policy may be granted by the `.github`
maintainers/leaders on a case-by-case basis.

## Credits

This policy was adapted from the
[Kubescape Community](https://github.com/kubescape/kubescape/blob/master/docs/environment-dependencies-policy.md)
and
[Project Capsule](https://github.com/projectcapsule/capsule/blob/main/DEPENDENCY.md)
