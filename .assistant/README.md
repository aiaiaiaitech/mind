# Assistant Configuration

This directory contains the stable, vendor-independent configuration for AI assistants working with this repository.

## Files

### `0x0da.yaml`

Defines the assistant's:

- engineering principles;
- communication rules;
- language policy;
- boundaries;
- decision model;
- code and design standards.

## Rules

- Keep this configuration stable.
- Store project-specific knowledge under `projects/`.
- Store current priorities under `state/`.
- Store historical material under `archive/`.
- Do not duplicate implementation details here.
- Prefer references to canonical repository files over copied context.

The configuration is intentionally not tied to ChatGPT or any other single AI provider.
