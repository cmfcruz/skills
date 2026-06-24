---
name: finish-up
description: Use when code changes are believed complete and before reporting done, opening a PR, or handing work back. Use to review the diff, remove dead code, run checks, and verify claims. Do not use at the start of implementation.
---

# Finish Up

Close the loop before claiming completion.

## Steps

1. Review the diff for unrelated changes.
2. Remove dead code, commented-out code, unused imports, and obsolete tests.
3. Check for accidental duplication or inconsistent naming.
4. Run the most relevant checks.
5. Report what changed and what verification ran.

## Final Check

- Is the diff scoped to the task?
- Are claims backed by commands, tests, or file inspection?
- Are remaining risks or skipped checks stated clearly?

