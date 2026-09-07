# Git Cheatsheet

Adapt `<default-branch>`, `<branch>`, and commit text to the project.

## Inspect and branch

```shell
git status
git pull --ff-only
git switch -c <branch>
```

Use branch names such as `feature/add-export-flow`, `fix/123-handle-empty-input`, or `docs/update-workflow`.

## Review and commit

```shell
git status --short
git diff
git add <paths>
git diff --staged
git commit -m "<type>(<optional-scope>): <imperative summary>"
```

Examples: `feat(api): add export endpoint`, `fix: handle empty input`, `docs: clarify validation workflow`.

## Push and open a pull request

```shell
git push -u origin <branch>
```

Then create a pull request that links the issue and documents the solution, validation, risks, and documentation impact.

## Useful inspection

```shell
git log --oneline --decorate -n 10
git diff <default-branch>...HEAD
```
