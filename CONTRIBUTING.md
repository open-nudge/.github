<!--
SPDX-FileCopyrightText: © 2025 open-nudge <https://github.com/open-nudge>
SPDX-FileContributor: szymonmaszke <github@maszke.co>

SPDX-License-Identifier: Apache-2.0
-->

# Contributing guide

## Table of contents

- [General](#general)
- [Prerequisites](#prerequisites)
- [Contributions](#contributions)
    - [Committing changes](#committing-changes)
    - [Creating a pull request](#creating-a-pull-request)
    - [Merging pull requests](#merging-pull-requests)

## General

We welcome all contributions from the community.
Adhere to [Code of Conduct](./CODE_OF_CONDUCT.md) at all times.

## Prerequisites

1. Read [ROADMAP](ROADMAP.md) to understand the project's goals.
1. Read Developer's Certificate of Origin (DCO) in [DCO.md](DCO.md)
    (you must sign-off your PRs).
1. Read [LICENSE](LICENSE.md)

## Contributions

We welcome non-code contributions as well. If you have any suggestions,
ideas, or want to report a bug, follow these steps:

1. Verify open issues to see if someone reposrted similar
    issue or requested a similar feature.
1. If the issue exists, upvote it and share more information
    in a comment (use cases, examples and so on).
1. If the issue does not exist, create a new one from the
    Issues Templates tab.
1. Follow the appropriate template for the issue

### Committing changes

Please follow the simplified [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)
standard in every commit, for example:

```bash
git commit -s -S -m "feat: add new feature"
```

- You can __only use `fix`, `feat`, `fix!`, `feat!`__ types,
    __we do not accept any other types__ (e.g. `chore`, `refactor`, `docs` and
    others).
- Your commits should be atomic and should not contain many changes.
- __Your commits have to be signed-off (use `-s` flag in `git commit` as in
    the example above).__ Please see the [DCO](DCO.md) for more information.
- __Your commits have to be signed (use `-S` flag in `git commit` as in
    the example above).__ Please see the [Signing commits](https://docs.github.com/en/authentication/managing-commit-signature-verification/signing-commits)
    for more information.

### Creating a pull request

Follow [GitHub Flow](https://guides.github.com/introduction/flow/);
`main` branch should always be in the releasable state.

__Small pull requests are encouraged.__ If, for some reason,
you cannot make small a pull request, describe the reasons in the
`pull request` description.

Pull requests have to be:

- __Contain `type` akin to the commits__;
    Same rules apply (only `fix`, `feat`, `fix!`, `feat!` allowed)
- __Linked to the `issue`__ via `Closes #XXX`
    (where `XXX` is the issue number) in the description.
- Target the `main` branch.
- Contain descriptive header and (optionally) description.

<!-- vale off -->

> [!TIP]
> Type of the pull request should be the largest
> of all commits (`feat!` > `fix!` > `feat` > `fix`)

<!-- vale on -->

Other features:

- Pull requests will be automatically labeled based on the type of the commit
    (in some cases, you might want to manually add the label from the existing ones).
- __Stale pull requests__ (no changes for 7 days) will be automatically closed
    (can be reopened later).

> [!WARNING]
> Once you submit a PR, __do not rebase it__ (easier to review the changes).

### Merging pull requests

Maintainers will merge your pull request after it is approved.
In general, if `pre-commit` checks pass, no major changes should be necessary.

<!-- vale off -->

> [!NOTE]
> We use `Squash and Merge` strategy for merging pull requests, individual
> commits should not matter if they follow the guidelines.

<!-- vale on -->

If you need help with this part of the process, tag one of the maintainers
in the PR.
