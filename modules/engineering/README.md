# Engineering

Organization-wide engineering contracts that are stable across individual repositories.

## Principles

- keep core contracts vendor-independent;
- prefer explicit interfaces and versioned schemas;
- separate domain logic from providers, infrastructure, and delivery interfaces;
- test behavior at module boundaries;
- document operational assumptions near the code;
- require a green test and CI suite before publication.

Repository-specific architecture, commands, and deployment details remain in each repository and are referenced from this module.

## Dependencies

- `identity`
- `governance`
