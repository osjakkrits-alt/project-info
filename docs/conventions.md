# Conventions

These defaults apply until a project adopts more specific standards.

## General

- Prefer clear, consistent names over abbreviations.
- Keep modules and functions focused on one responsibility.
- Document intent and constraints rather than restating implementation.
- Avoid secrets, personal data, and environment-specific values in version control.

## Files and formatting

- Use UTF-8, final newlines, and the formatter selected by the project.
- Use lowercase kebab-case for documentation file names unless an ecosystem requires otherwise.
- Keep generated files separate and document how to reproduce them.

## Testing

- Add or update tests for behavior changes.
- Cover expected behavior, edge cases, and failure paths proportionate to risk.
- Keep tests deterministic and independent of private local state.

## Git

- Follow branch naming and Conventional Commit guidance in `docs/workflow.md`.
- Keep commits scoped and avoid mixing unrelated formatting or refactoring.

## Project-specific additions

Add language, API, database, accessibility, observability, and security conventions here once selected.
