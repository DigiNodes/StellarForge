# StellarForge Repository Map

This file is the canonical project-level map of StellarForge repositories and planned modules.

## Active Repositories

### StellarForge

**Repository:** `DigiNodes/StellarForge`  
**State:** Active — Governance  
**Responsibility:** Project governance, roadmap, repository map, cross-repository architecture, shared policies, and decision records.

This repository does not own component implementation backlogs.

### stellarforge-cli

**Repository:** [DigiNodes/stellarforge-cli](https://github.com/DigiNodes/stellarforge-cli)  
**State:** Active  
**Responsibility:** CLI foundation, project generation, templates, environment diagnostics, development orchestration, testing, configuration, and deployment tooling.

## Planned Repositories

The following names represent planned responsibility areas. They are not active repositories at the time of this document.

| Planned repository | Intended responsibility |
| --- | --- |
| `stellarforge-sdk` | Reusable application-facing Stellar/Soroban libraries and adapters |
| `stellarforge-workflows` | Workflow orchestration and reusable automation primitives |
| `stellarforge-indexer` | Stellar/Soroban event ingestion, indexing, storage, and query infrastructure |
| `stellarforge-security` | Security analysis, validation, testing, and hardening tooling |
| `stellarforge-examples` | Reference applications and supported integration examples |

## Repository Creation Gate

A planned repository should move to Incubating only when Project Maintainers have approved:

1. its responsibility and non-overlap with existing modules;
2. maintainer ownership;
3. initial architecture and public interfaces;
4. security assumptions and trust boundaries;
5. development/release expectations;
6. the initial foundation work.

## Repository Responsibilities

Every active implementation repository should eventually maintain, as applicable:

- a clear README and scope;
- contribution guidance;
- code of conduct reference;
- security policy;
- license;
- architecture documentation;
- automated quality checks;
- release/versioning policy;
- maintainer or ownership rules.

## Cross-Repository Changes

When a change affects multiple components, the shared decision should be recorded in this governance repository. Implementation work should then be performed in each affected component repository.

This avoids duplicating implementation backlogs in the governance repository while preserving a durable record of project-wide decisions.
