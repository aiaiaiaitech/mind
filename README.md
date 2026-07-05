# mind

> Personal knowledge repository.
> Single source of truth for AI assistants.

## Purpose

This repository stores long-term knowledge, stable preferences, specifications, and project context in a structured Markdown format.

The goal is to provide one canonical knowledge base that can be consumed by multiple AI systems instead of duplicating prompts or instructions across different platforms.

Create a vendor-independent personal knowledge repository that becomes the single source of truth for multiple AI systems (ChatGPT, Claude Code, GitHub Copilot, Cursor, Grok, Gemini, etc.), instead of duplicating prompts and instructions across different platforms.

## Core Idea

Move from prompt engineering to context engineering.

Instead of storing knowledge inside individual AI clients, maintain one structured Git repository containing stable knowledge, specifications, and project context.

Every AI assistant should consume the same repository.

## Principles

- One source of truth.
- One topic per file.
- Markdown first.
- Git versioning.
- Human readable.
- AI friendly.

## Repository Structure

```
identity/
knowledge/
systems/
projects/
state/
archive/
```

## Categories

### identity
ф
Stable information describing the owner.

Examples:

- language preferences
- communication style
- writing conventions

### knowledge

Domain knowledge and long-term documentation.

### systems

Reusable systems and specifications.

Examples:

- marker system
- branding
- workflows

### projects

Project-specific context.

Each project should be self-contained.

### state

Current priorities and active work.

Unlike the rest of the repository, this section changes frequently.

### archive

Historical information that should not influence current work.

## Design Rules

- Avoid duplicated information.
- Every concept has exactly one canonical location.
- Cross-reference instead of copying.
- Keep files focused.
- Prefer specifications over notes.

## License

Private repository.