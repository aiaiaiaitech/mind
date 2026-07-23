# AGENTS

This repository is the primary source of context for its Mind implementation.

## Purpose

Use this repository as the canonical knowledge base before relying on assumptions or inferred context.

Prefer explicit repository contracts over conventions that are not declared by the repository.

## Entry Point

Start with `manifest.yaml`.

The manifest defines:

- the Mind kind and owner
- registered modules
- module loading order
- optional context
- validation schema

Do not assume a fixed repository layout. Personal, organizational, and future Mind implementations may register different modules while sharing the same baseline contract.

## Loading Rules

- Read only the files relevant to the current task.
- Follow the module and loading declarations in `manifest.yaml`.
- Do not load the entire repository unless explicitly requested.
- Treat registered Markdown documents as specifications unless they state otherwise.
- Load archived context only when explicitly requested or required to resolve history.
- Avoid duplicating information in generated outputs.

## Source Precedence

Each concept must have exactly one canonical source.

When multiple files overlap or conflict:

1. follow explicit precedence declared by `manifest.yaml` or the relevant module contract
2. prefer the dedicated canonical specification for the concept
3. prefer stable context over transient context unless the task concerns current state
4. do not merge conflicting rules automatically
5. surface unresolved conflicts clearly

File modification time alone does not establish authority.

## Module Boundaries

- Respect each module's declared responsibility.
- Do not introduce undeclared dependencies between modules.
- Prefer cross-references over duplicated content.
- Keep modules independently replaceable where the contract permits it.
- Do not invent new systems when an existing registered module already owns the concern.

## Safety and Integrity

- Never add secrets, credentials, private keys, access tokens, or personal sensitive data unless the repository explicitly defines a secure external reference mechanism.
- Preserve existing terminology and repository conventions.
- Keep generated changes human-readable and compatible with the declared validation schema.
- Do not reinterpret an abstract baseline as a concrete personal or organizational implementation.

## Output

When generating or modifying repository content:

- state the relevant source or contract used
- preserve canonical ownership
- keep changes minimal and task-scoped
- update references when canonical paths change
- report ambiguity instead of silently guessing
