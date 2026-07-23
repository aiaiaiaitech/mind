# modules

A module is a focused, replaceable unit of context composed into a concrete mind.

## Interface

Each module should declare:

- `id` — stable unique identifier;
- `purpose` — one responsibility;
- `stability` — `stable`, `transient`, or `archived`;
- `dependencies` — explicit module identifiers;
- `entrypoints` — canonical files loaded by consumers;
- `owner` — entity responsible for the module;
- `visibility` — public or private handling expectations.

## Rules

- A module must have one reason to change.
- A module must not duplicate another module's canonical content.
- Dependencies must point toward abstractions or stable contracts.
- Cyclic dependencies are forbidden.
- Optional consumers must be able to ignore the module safely.
- Concrete implementations may choose any folder names; registration belongs in `manifest.yaml`.

## Example registration

```yaml
modules:
  registered:
    - identity
    - engineering

module_contracts:
  identity:
    purpose: describe the owning entity
    stability: stable
    dependencies: []
    entrypoints:
      - identity/README.md
```

The example is illustrative and is not required by the baseline.