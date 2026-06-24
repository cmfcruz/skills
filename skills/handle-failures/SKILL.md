---
name: handle-failures
description: Use during writing when adding catch blocks, error branches, retries, validation failures, fallbacks, or user-facing failure messages. Do not use when no failure path is being changed.
---

# Handle Failures

Make failures explicit, actionable, and consistent with the surrounding code.

## Rules

1. Do not silently swallow errors.
2. Either handle the error, rethrow with useful context, or document why ignoring
   it is correct.
3. Preserve original error details when they help debugging.
4. Match the repository's existing error style: find a nearby error path and
   mirror its error type, logging call, and message format.
5. For user-facing failures, write an actionable message and keep internal
   details — stack traces, secrets, identifiers — out of it; log those instead.
6. For retries, bound the attempts and do not retry errors that cannot succeed
   on retry.
7. For fallbacks, do not let the fallback hide that the primary path failed;
   record it.
8. Include tests for the failure paths you add or change.

## Final Check

- Can a developer understand what failed and why?
- Is the failure observable in logs, return values, UI, or tests?
- Do user-facing messages keep internal and sensitive detail out?
