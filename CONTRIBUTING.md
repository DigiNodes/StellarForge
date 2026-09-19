# Contributing to StellarForge

Thank you for helping improve StellarForge.

## Choose the right repository

This repository is the **governance and coordination repository**. It is not the primary contributor task backlog.

Use a component repository for implementation work. The currently active implementation repository is:

- [stellarforge-cli](https://github.com/DigiNodes/stellarforge-cli)

Planned repositories are listed in [REPOSITORIES.md](./REPOSITORIES.md), but should not be treated as active until they are created and approved.

## Changes appropriate for this repository

Open a focused pull request here for:

- project governance;
- roadmap changes;
- repository lifecycle or ownership;
- cross-repository architecture;
- shared security or release policy;
- project-level decision records;
- corrections to the canonical repository map.

Implementation bugs, feature tasks, tests, and contributor assignments belong in the owning component repository.

## Governance change workflow

1. Create a short-lived branch from `main`.
2. Update the smallest relevant governance documents.
3. Explain the rationale and affected repositories in the pull request.
4. Identify security or compatibility implications when applicable.
5. Obtain Project Maintainer review for material changes.
6. Merge only when the documentation accurately reflects active project state.

Governance changes do **not** require a matching GitHub issue. The pull request itself may be the proposal and review record.

## Cross-repository proposals

For a material project-level decision, add a decision record under `docs/decisions/` using the format described in [docs/decisions/README.md](./docs/decisions/README.md).

Once approved, implementation tasks should be created only in the affected component repositories when contributor work is actually needed.

## Pull Request Expectations

A governance PR should:

- have one coherent purpose;
- distinguish active capabilities from planned work;
- use verified links for active repositories;
- avoid promising dates that have not been approved;
- keep secrets and private operational details out of public documentation;
- update related governance documents when a decision changes them.

## Code of Conduct

All project participation is governed by [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md).

## Security

Do not disclose vulnerabilities in a public governance PR. Follow [SECURITY.md](./SECURITY.md) and report vulnerabilities privately to the affected implementation repository.
