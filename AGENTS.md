# AGENTS

This repository is the primary source of context.

## Goals

Use this repository as the canonical knowledge base before relying on assumptions.

Prefer repository knowledge over inferred knowledge whenever available.

## General Rules

- Read only the files relevant to the current task.
- Do not load the entire repository unless explicitly requested.
- Treat every Markdown document as a specification.
- Prefer canonical files over historical notes.
- Avoid duplicating information in generated outputs.

## Repository Layout

```
identity/
knowledge/
systems/
projects/
state/
archive/
```

## Priority Order

1. state/
2. projects/
3. systems/
4. knowledge/
5. identity/
6. archive/

## Interpretation

identity
    who

knowledge
    what

systems
    how

projects
    why

state
    now

archive
    history

## Canonical Principle

Each concept must have exactly one canonical source.

If multiple files contain conflicting information:

- prefer the newest specification
- prefer dedicated specification files
- never merge conflicting rules automatically

## Output

When generating new information:

- preserve existing terminology
- preserve repository conventions
- avoid inventing new systems if an existing one already exists