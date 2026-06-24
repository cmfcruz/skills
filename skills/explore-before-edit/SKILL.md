---
name: explore-before-edit
phase: before-writing
description: Use before writing new code in an unfamiliar area, adding a helper, introducing a pattern, or answering implementation questions that require repository context. For changing existing behavior with callers, use refactor-safely instead. Do not use for pure prose, scheduling, or questions that do not require codebase inspection.
---

# Explore Before Edit

Before writing code, inspect the surrounding implementation so new work fits the
project instead of inventing a second style.

## Steps

1. Identify the target files, nearby modules, and likely tests.
2. Search for existing helpers, types, patterns, names, and error handling.
3. Read the closest examples before editing.
4. Prefer existing conventions over new abstractions.
5. State the local pattern you are following before making substantial changes.

## Final Check

- Did you inspect before editing?
- Did you reuse an existing helper or pattern when one already existed?
- Did you avoid adding a new convention where the repo already had one?

