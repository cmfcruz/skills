---
name: explore-before-edit
description: Use before writing new code in an unfamiliar area, adding a helper, introducing a pattern, or answering implementation questions that require repository context. For changing existing behavior with callers, use refactor-safely instead. Do not use for pure prose, scheduling, or questions that do not require codebase inspection.
---

# Explore Before Edit

Before writing code, inspect the surrounding implementation so new work fits the
project instead of inventing a second style.

## Steps

1. Identify the target files, nearby modules, and likely tests.
2. Search for existing helpers, types, patterns, names, and error handling with
   targeted text search.
3. Read the nearest definition plus one or two callers or sibling examples
   before editing.
4. Prefer existing conventions over new abstractions.
5. Stop once you can name the local pattern and likely blast radius.
6. State the local pattern you are following before making substantial changes.

## When Not To Use

Do not use this skill to justify broad exploration for a trivial or localized
change where the pattern is already obvious. Explore in proportion to the
change's blast radius.

## Final Check

- Did you inspect before editing?
- Can you name the local pattern and likely blast radius?
- Did you avoid reading beyond what the change needs?
