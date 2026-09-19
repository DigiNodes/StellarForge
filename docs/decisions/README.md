# Project Decision Records

This directory records decisions that affect StellarForge across repository boundaries.

## When a project decision record is required

Create a project-level decision record when a proposal changes one or more of the following:

- repository boundaries or ownership;
- shared public interfaces;
- project-wide security assumptions;
- supported network policy;
- release/version compatibility between components;
- licensing strategy;
- governance or maintainer authority;
- lifecycle of an official repository.

Component-local implementation decisions belong in that component repository.

## Suggested format

```markdown
# SFD-XXXX — Decision title

Status: Proposed | Accepted | Superseded
Date: YYYY-MM-DD

## Context

## Decision

## Affected repositories

## Security implications

## Compatibility / migration

## Consequences
```

Decision records are merged through governance pull requests and should not be silently rewritten after acceptance. If a decision changes materially, add a new record and mark the old record superseded.
