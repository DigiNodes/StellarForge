# StellarForge Governance

## Purpose

This repository is the governance and coordination layer for the StellarForge project. It exists to keep cross-repository direction explicit without turning project governance into a contributor issue queue.

Implementation work belongs in component repositories such as `stellarforge-cli`.

## Governance Principles

1. **Architecture before expansion.** New repositories and major modules should have a defined responsibility, interfaces, security boundary, and maintainer ownership before implementation begins.
2. **Decisions are recorded.** Material cross-repository decisions should be documented in this repository through pull requests and decision records.
3. **Implementation stays local.** Code-level tasks, bugs, and contributor issues belong in the repository that owns the code.
4. **Security is a project property.** Each component owns its implementation controls, while this repository defines shared expectations.
5. **Stable contracts over coordination by convention.** Cross-repository integrations should rely on documented interfaces and versions.
6. **No hidden production authority.** Releases, signing, publishing, deployment credentials, and emergency controls must be explicitly owned and auditable.

## Roles

### Project Maintainers

Project Maintainers steward StellarForge as a whole. They may:

- approve project direction and roadmap changes;
- approve creation, transfer, archival, or renaming of official repositories;
- approve cross-repository architecture decisions;
- define shared security and release expectations;
- appoint or remove Component Maintainers;
- resolve cross-component ownership conflicts.

### Component Maintainers

Component Maintainers are responsible for one implementation repository or module. They may:

- maintain its implementation backlog;
- review and merge changes under that repository's rules;
- maintain tests, CI, releases, and documentation;
- propose changes to shared contracts.

Component Maintainers should not unilaterally change another component's public contract or a project-wide governance decision.

### Contributors

Contributors participate through component repositories and their local contribution policies. Contribution does not automatically grant release, administrative, signing, or governance authority.

## Decision Classes

### Local implementation decisions

Changes confined to one component and not affecting shared contracts are decided in that component repository.

Examples include internal refactors, tests, implementation bugs, and component-specific developer experience.

### Cross-repository decisions

Changes affecting more than one component, public interfaces between components, repository structure, shared security policy, or release coordination should be documented here.

A cross-repository proposal should describe:

- context and problem;
- decision;
- affected repositories;
- compatibility implications;
- security implications;
- migration or rollout plan when applicable.

### Foundational decisions

Repository creation/archival, licensing strategy, governance model, supported network policy, project-wide release policy, and other foundational decisions require explicit Project Maintainer approval.

## Decision Process

The default governance workflow is:

```text
Proposal
   |
   v
Focused governance PR
   |
   v
Maintainer review
   |
   +--> revision when needed
   |
   v
Approval and merge
   |
   v
Implementation in component repositories
```

Routine governance updates may be merged directly by authorized maintainers when they only synchronize documentation with an already-approved state.

## Repository Lifecycle

Official repositories move through these states:

- **Planned** — scope is recognized but implementation repository is not yet active.
- **Incubating** — repository exists and foundational architecture is being established.
- **Active** — repository has maintainers, documented scope, security policy, and maintained implementation.
- **Maintenance** — feature development is limited but supported releases/fixes continue.
- **Archived** — repository is read-only or otherwise retired.

Creating a new repository should require:

- a clear problem and responsibility;
- defined relationship to existing modules;
- named maintainer ownership;
- initial security model;
- expected public interfaces;
- a foundation plan.

## Branch and Change Management

Governance changes should normally use short-lived branches and pull requests into `main`.

For this repository:

- governance documents should be reviewed for consistency with active component repositories;
- changes must not claim planned repositories or capabilities already exist when they do not;
- links to component repositories should be verified before merge;
- implementation task issues should not be created here merely to mirror component backlogs.

## Security and Releases

Each implementation repository owns its release pipeline and secrets. Shared expectations include:

- least-privilege automation;
- protected release environments where applicable;
- reproducible dependency installation;
- no secrets in pull-request workflows;
- auditable versioning and release notes;
- private vulnerability reporting.

Project governance must never require contributors to expose wallet keys, signing secrets, tokens, or production credentials.

## Amendments

This governance model may be changed through a focused pull request approved by Project Maintainers. Material changes should explain why the previous model is insufficient and identify affected repositories.
