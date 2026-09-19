# StellarForge

> Open infrastructure for building production-ready applications on Stellar.

StellarForge is an open-source infrastructure initiative for reusable developer tooling, workflows, indexing, security modules, SDKs, templates, and reference applications for the Stellar ecosystem.

This repository is the **governance and coordination repository** for StellarForge. It defines the project direction, architecture boundaries, repository map, roadmap, decision process, security expectations, and shared project policies. Product implementation belongs in the relevant component repositories.

## Current Status

StellarForge is in its foundation/MVP stage.

The first implementation repository is **[stellarforge-cli](https://github.com/DigiNodes/stellarforge-cli)**. The CLI is the initial developer entry point for project scaffolding, environment diagnostics, local development, testing, and guarded Stellar Testnet deployment.

Other planned modules remain roadmap items until their repositories are created and their architecture is approved.

## Vision

StellarForge aims to reduce repeated infrastructure work when teams build on Stellar by providing composable, secure, well-documented building blocks.

The project is designed around several principles:

- **Modularity** — components should be independently usable and replaceable.
- **Security by default** — secrets, signing material, network access, and automation require explicit boundaries.
- **Deterministic developer experience** — project generation, testing, and workflows should behave predictably across supported environments.
- **Progressive adoption** — developers should be able to use one module without adopting the entire platform.
- **Open governance** — material architectural and project-level decisions should be recorded and reviewable.

## Project Architecture

```text
                         StellarForge
                Governance & Coordination Layer
                             |
        +--------------------+--------------------+
        |                    |                    |
        v                    v                    v
  Developer Tooling    Runtime Libraries    Infrastructure
        |                    |                    |
  stellarforge-cli      SDKs / adapters      Workflows
  Templates             Wallet helpers       Indexer
  Project tooling       API primitives        Security tooling
        |                    |                    |
        +--------------------+--------------------+
                             |
                             v
                    Stellar / Soroban
```

The architecture is intentionally modular. Not every planned module exists yet.

## Repository Map

| Repository | Status | Responsibility |
| --- | --- | --- |
| [stellarforge-cli](https://github.com/DigiNodes/stellarforge-cli) | Active | CLI, project generation, diagnostics, local development, testing, deployment tooling |
| stellarforge-sdk | Planned | Reusable Stellar/Soroban application libraries and adapters |
| stellarforge-workflows | Planned | Workflow orchestration and reusable automation primitives |
| stellarforge-indexer | Planned | Event ingestion, indexing, query, and storage infrastructure |
| stellarforge-security | Planned | Security analysis, validation, testing, and hardening tooling |
| stellarforge-examples | Planned | Reference applications and integration examples |

A planned repository name is not a promise that the repository already exists. New implementation repositories should be created only after their scope and ownership are sufficiently defined.

See [REPOSITORIES.md](./REPOSITORIES.md) for repository lifecycle and ownership rules.

## Roadmap

The project roadmap is maintained in [ROADMAP.md](./ROADMAP.md).

At a high level:

1. **Foundation and CLI MVP** — establish governance and deliver the first production-oriented developer interface.
2. **SDK foundation** — define reusable application-facing APIs after CLI contracts stabilize.
3. **Workflow and indexing infrastructure** — add reusable runtime infrastructure with explicit operational boundaries.
4. **Security and reference ecosystem** — expand security tooling, examples, integrations, and ecosystem maturity.

Roadmap phases describe direction, not guaranteed delivery dates.

## Governance

Project-level decisions are maintained here rather than as contribution issues.

- [GOVERNANCE.md](./GOVERNANCE.md) — roles, authority, decision process, and repository lifecycle.
- [docs/architecture/README.md](./docs/architecture/README.md) — architecture principles and cross-repository boundaries.
- [docs/decisions/README.md](./docs/decisions/README.md) — project-level decision records.
- [REPOSITORIES.md](./REPOSITORIES.md) — official and planned repositories.
- [ROADMAP.md](./ROADMAP.md) — phased project direction.

Implementation issues belong in the component repository where the code lives. This governance repository is not intended to maintain a contributor task backlog.

## Contributing

Start with [CONTRIBUTING.md](./CONTRIBUTING.md).

For implementation work, use the relevant component repository and its contribution workflow. For governance, architecture, roadmap, or cross-repository policy changes, propose a focused pull request to this repository with the rationale and affected modules.

All participants must follow the [Code of Conduct](./CODE_OF_CONDUCT.md).

## Security

Please do not open public issues for vulnerabilities. Follow [SECURITY.md](./SECURITY.md) and use GitHub's private vulnerability reporting for the affected implementation repository.

## License

Component repositories define their own license files. The active CLI repository currently uses the MIT License. This governance repository should not be assumed to grant a license until a root license file is explicitly adopted.
