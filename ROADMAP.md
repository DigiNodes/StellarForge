# StellarForge Roadmap

This roadmap describes project direction. It is not a delivery-date commitment.

## Phase 0 — Governance and Foundation

**Status: Active**

Objectives:

- establish the governance repository as the project coordination layer;
- define repository lifecycle and ownership;
- define cross-repository architecture principles;
- establish shared security expectations;
- keep planned modules distinct from active implementations.

Exit criteria:

- governance, roadmap, repository map, security policy, and architecture principles are documented;
- the first component repository has an explicit scope and maintained foundation.

## Phase 1 — CLI MVP

**Status: Active**

Primary repository: [stellarforge-cli](https://github.com/DigiNodes/stellarforge-cli)

Objectives:

- production-oriented TypeScript CLI foundation;
- project scaffolding and controlled starter templates;
- environment diagnostics;
- local development orchestration;
- unified project testing;
- guarded Stellar Testnet deployment;
- deterministic configuration;
- cross-platform CI and end-to-end smoke validation;
- protected release/versioning workflow.

The CLI is the first StellarForge implementation because it establishes the developer-facing contracts that later modules can integrate with.

## Phase 2 — SDK Foundation

**Status: Planned**

Objectives:

- define SDK responsibility and package boundaries;
- document supported Stellar/Soroban APIs;
- establish wallet/signing abstractions without taking custody of secrets;
- provide reusable transaction and contract interaction primitives;
- define compatibility/versioning policy with CLI-generated projects.

The SDK repository should not be created merely to satisfy the roadmap. Its initial public API and ownership should be approved first.

## Phase 3 — Workflow and Indexing Infrastructure

**Status: Planned**

Objectives:

- reusable workflow execution primitives;
- event ingestion and indexing architecture;
- idempotency and replay semantics;
- storage abstraction and operational observability;
- clear boundaries between application workflows and chain data.

## Phase 4 — Security and Reference Ecosystem

**Status: Planned**

Objectives:

- reusable contract/application security tooling;
- reference applications demonstrating supported integration patterns;
- security baselines and validation packs;
- broader documentation and ecosystem integrations.

## Cross-Cutting Tracks

These apply across all phases:

### Security

Threat modeling, least privilege, secret isolation, dependency controls, secure release automation, and responsible disclosure.

### Developer Experience

Predictable commands, actionable errors, stable configuration, high-quality documentation, and cross-platform support.

### Architecture

Documented interfaces, explicit ownership, backwards-compatibility decisions, and modular adoption.

### Governance

Repository lifecycle, maintainer responsibilities, decision records, roadmap synchronization, and transparent project direction.

## Roadmap Change Policy

A material roadmap change should be made through a governance pull request explaining:

- what changed;
- why it changed;
- which repositories are affected;
- whether public contracts or compatibility expectations change.
