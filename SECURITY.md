# StellarForge Security Policy

Security is a shared StellarForge responsibility. This repository defines project-level expectations; each implementation repository owns its component-specific security controls and vulnerability handling.

## Reporting a Vulnerability

Do **not** open a public issue or governance pull request for a suspected vulnerability.

Report the vulnerability privately through GitHub Private Vulnerability Reporting / Security Advisories in the affected implementation repository.

For the active CLI, report against:

- [DigiNodes/stellarforge-cli](https://github.com/DigiNodes/stellarforge-cli)

If the affected component cannot be identified, contact a Project Maintainer privately and provide only the minimum information necessary to route the report.

## Scope

This policy applies to official StellarForge repositories and project-controlled modules.

Currently active:

- `DigiNodes/StellarForge` — governance and coordination;
- `DigiNodes/stellarforge-cli` — CLI implementation.

Other module names in the roadmap are planned and should not be treated as active repositories until listed as active in [REPOSITORIES.md](./REPOSITORIES.md).

## Shared Security Expectations

Implementation repositories should adopt controls appropriate to their risk, including:

- least-privilege GitHub Actions permissions;
- pinned or otherwise controlled CI dependencies;
- reproducible dependency installation;
- no secrets in pull-request workflows;
- protected release credentials/environments;
- safe subprocess handling;
- explicit network selection for sensitive operations;
- no logging of private keys, seed phrases, tokens, or credentials;
- dependency and static-analysis checks where supported;
- documented vulnerability response.

## Stellar-Specific Boundaries

StellarForge should avoid taking custody of signing material unless a future component explicitly requires and documents that responsibility.

Developer tooling should prefer named identities managed by established Stellar tooling over accepting raw private keys or seed phrases.

Mainnet-sensitive actions must be explicit and separately reviewed; Mainnet must not become an accidental default.

## Coordinated Response

Maintainers should:

1. acknowledge and triage a private report;
2. identify affected repositories and versions;
3. limit disclosure while remediation is in progress;
4. prepare and validate a fix;
5. publish advisories and upgrade guidance when appropriate;
6. coordinate fixes across repositories when a shared contract is affected.

## Supported Versions

Each implementation repository defines its own supported versions. This governance repository does not override component support windows.
