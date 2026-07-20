# mind

> Personal knowledge repository.
> Single source of truth for AI assistants.

## Purpose

`mind` is a vendor-independent knowledge base for stable preferences, specifications, project context, and current state.

It allows ChatGPT, Claude Code, GitHub Copilot, Cursor, Grok, Gemini, and other assistants to consume the same canonical context instead of maintaining duplicated prompts across platforms.

## Core Idea

Move from prompt engineering to context engineering.

Knowledge should live in a structured, versioned repository rather than inside individual AI clients.

## Principles

- One source of truth.
- One topic per file.
- Markdown first for knowledge.
- YAML for machine-readable assistant configuration.
- Git versioning.
- Human readable.
- AI friendly.

## Repository Structure

```text
.assistant/
identity/
knowledge/
systems/
projects/
state/
archive/
```

## Categories

### `.assistant`

Stable, vendor-independent assistant configuration.

The canonical configuration is `.assistant/0x0da.yaml`. Project implementation details do not belong there.

### `identity`

Stable information describing the owner, including language preferences, communication style, and writing conventions.

### `knowledge`

Domain knowledge and long-term documentation.

### `systems`

Reusable systems, specifications, branding, and workflows.

### `projects`

Project-specific context. Each project should remain self-contained.

### `state`

Current priorities and active work. Unlike most of the repository, this section changes frequently.

### `archive`

Historical information that should not influence current work unless referenced explicitly.

## Design Rules

- Avoid duplicated information.
- Give every concept one canonical location.
- Cross-reference instead of copying.
- Keep files focused.
- Prefer specifications over loose notes.
- Separate stable knowledge from temporary state.
- Keep assistant behavior separate from project implementation details.

## Visibility

This repository is public. Do not commit secrets, credentials, private health data, or other sensitive material.
