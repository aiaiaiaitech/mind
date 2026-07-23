# mind

> A versioned context repository for humans and AI systems.

## Purpose

`mind` is a vendor-independent source of truth for structured context. It defines a small reusable contract that can later specialize into a personal, organization, project, or product mind.

The baseline intentionally avoids prescribing domain-specific folders. Concrete implementations compose only the modules they need.

## Contract

Every compatible mind must:

- declare an explicit owner and context version;
- keep one canonical location for each concept;
- separate stable context from transient state;
- keep modules focused and independently replaceable;
- declare module dependencies explicitly;
- prefer references over duplicated content;
- remain readable by humans and machines;
- contain no secrets or private credentials.

## Architecture

```text
Mind
├── manifest.yaml
├── schema/
│   └── mind.schema.json
└── modules/
    └── README.md
```

`Mind` is the abstraction. A repository becomes a concrete implementation by composing modules such as identity, assistant policy, governance, engineering, knowledge, systems, or state.

Examples:

```text
PersonalMind = Identity + Assistant + Knowledge + Systems + State
OrganizationMind = Identity + Governance + Engineering + Portfolio + Decisions
```

The baseline does not require these modules and does not define their internal content.

## Design Principles

- **Single Responsibility:** one purpose per module and one topic per file.
- **Open/Closed:** new mind types are added through modules, not by changing the baseline contract.
- **Liskov Substitution:** every concrete mind satisfies the same manifest and validation invariants.
- **Interface Segregation:** consumers load only the modules they need.
- **Dependency Inversion:** concrete modules depend on the baseline contract; the baseline never depends on concrete modules.
- Composition is preferred over inheritance.
- Contracts are preferred over conventions that cannot be validated.

## Lifecycle

1. Build and validate a neutral baseline snapshot.
2. Tag and release that snapshot.
3. Fork it into another account or organization.
4. Evolve each repository independently as a concrete mind.
5. Share later neutral improvements only through explicit commits or versioned specifications.

## Visibility

This repository may be public. Never commit secrets, credentials, private health data, access tokens, or other sensitive material.