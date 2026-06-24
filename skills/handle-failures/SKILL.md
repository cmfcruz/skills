---
name: handle-failures
phase: during-writing
description: Use during writing when adding catch blocks, error branches, retries, validation failures, fallbacks, or user-facing failure messages. Do not use when no failure path is being changed.
---

# Handle Failures

Make failures explicit, actionable, and consistent with the surrounding code.

## Rules

1. Do not silently swallow errors.
2. Either handle the error, rethrow with useful context, or document why ignoring
   it is correct.
3. Preserve original error details when they help debugging.
4. Match the repository's existing error style.
5. Include tests for important failure paths.

## Final Check

- Can a developer understand what failed and why?
- Is the failure observable in logs, return values, UI, or tests?
- Did you avoid hiding unexpected states?

