# StellarForge Architecture Principles

This directory contains project-level architecture guidance. Component-specific ADRs remain in the component repository unless a decision changes a shared StellarForge contract.

## Architectural Goals

StellarForge should be:

- modular rather than monolithic;
- usable incrementally;
- deterministic where developer tooling permits;
- explicit about network and signing boundaries;
- secure by default;
- observable and testable;
- compatible through documented interfaces rather than shared internal state.

## Layering

The project is organized conceptually into:

1. **Developer experience** — CLI, generators, templates, documentation.
2. **Application libraries** — SDKs, adapters, wallet and API primitives.
3. **Infrastructure** — workflows, indexing, scheduling, storage.
4. **Security** — validation, analysis, testing, hardening.
5. **Stellar/Soroban** — external network and contract runtime.

Dependencies should generally flow downward. Infrastructure modules should not depend on application-specific UI concerns, and shared libraries should not depend on CLI internals.

## Security Boundaries

### Signing material

StellarForge components should not invent new secret-storage mechanisms when established Stellar tooling can own signing identities. Raw private keys and seed phrases should not be accepted as convenient configuration values.

### Network selection

Network-sensitive operations should require explicit network intent. Production/Mainnet behavior must not be an accidental default.

### Process execution

Developer tooling should prefer explicit executable and argument arrays rather than shell interpolation. Child-process lifecycle and environment inheritance should be bounded.

### Configuration

Configuration formats should be deterministic, versioned where compatibility matters, and should avoid executing arbitrary project code merely to read settings.

## Cross-Repository Contracts

A public contract between StellarForge repositories should define:

- owner;
- inputs and outputs;
- versioning expectations;
- error behavior;
- security assumptions;
- compatibility/migration policy.

Cross-repository contracts should not rely on unpublished source internals.

## Decision Records

Use [../decisions/README.md](../decisions/README.md) for decisions that materially affect more than one repository. Component-local implementation decisions should remain in that component's ADR collection.
