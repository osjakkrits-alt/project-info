# Development Workflow

Use this workflow for every planned change:

GitHub Issue / Sprint
→ Choose Prompt Template
→ Customize Prompt
→ Run Codex
→ Review Implementation
→ Run Validation
→ Update Documentation (optional)
→ Review Git Diff (optional)
→ Commit
→ Push
→ Create Pull Request
→ Merge
→ Close Issue

## Working agreement

1. Define scope and acceptance criteria in a GitHub issue or sprint.
2. Create a short-lived branch from the current default branch.
3. Use a prompt in `docs/ai/codex/templates/`, filling every relevant placeholder.
4. Review generated changes and run all available validation before committing.
5. Open a focused pull request linked to the issue, address review feedback, then merge and close the issue.

## Branch naming

Use lowercase kebab-case with a category and short description:

- `feature/add-export-flow`
- `fix/handle-empty-input`
- `docs/update-architecture`
- `chore/refresh-tooling`
- `refactor/simplify-validation`

Include an issue number when useful, for example `fix/123-handle-empty-input`.

## Commits

Use Conventional Commits:

```text
<type>(<optional-scope>): <imperative summary>
```

Common types are `feat`, `fix`, `docs`, `test`, `refactor`, `build`, `ci`, and `chore`. Keep each commit focused, explain breaking changes in the footer, and reference issues when helpful.

## Pull requests

Describe the problem, solution, validation, documentation impact, and remaining risks. Prefer a small reviewable diff and do not merge with unresolved required checks.
