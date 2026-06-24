---
name: conventional-commits
description: Use when preparing, naming, reviewing, or creating commits for completed code or documentation changes. Do not use during implementation unless the user asks for commit planning.
---

# Conventional Commits

Create small, meaningful commits with conventional messages.

## Format

Use:

```text
type(scope): summary
```

Common types:

- `feat`: user-visible feature
- `fix`: bug fix
- `refactor`: behavior-preserving code change
- `test`: test-only change
- `docs`: documentation-only change
- `chore`: maintenance

## Rules

1. Keep commits atomic and reviewable.
2. Choose the narrowest accurate type.
3. Use a scope when it clarifies the affected area.
4. Write the summary in imperative mood.
5. Do not hide behavior changes in `refactor` or `chore`.

## Final Check

- Does the commit message match the actual diff?
- Is the commit small enough to review?
- Would the type make sense in a changelog?
