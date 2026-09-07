# Using Codex

Codex can help implement, review, and validate scoped repository changes. It does not replace human review or project-specific quality gates.

## Recommended use

1. Start from a clear GitHub issue or sprint item.
2. Choose a template from `templates/` or the index in `prompt-library.md`.
3. Replace placeholders with repository paths, acceptance criteria, and validation commands.
4. Ask Codex to inspect existing instructions before editing.
5. Review the implementation, diff, and validation results before committing.

## Prompt hygiene

- State the outcome and boundaries explicitly.
- Provide acceptance criteria and known constraints.
- Name files or areas that must not change.
- Require reporting of failed or unavailable checks.
- Never include credentials, tokens, private keys, or sensitive production data.

See `git-cheatsheet.md` for the Git steps surrounding a Codex session.
