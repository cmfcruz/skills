---
name: write-tests
description: Use during writing when adding, changing, or repairing tests for code behavior. Use before refactors that need a safety net. Do not use for snapshot churn or tests that only mirror implementation details.
---

# Write Tests

Test observable behavior, not private implementation trivia.

## Rules

1. Start from the behavior the user or caller depends on.
2. Prefer real inputs and outputs over mocks when practical.
3. Mock only boundaries that are slow, external, nondeterministic, or unsafe.
4. Cover meaningful success and failure paths.
5. Make tests readable enough to explain the expected behavior.

## Final Check

- Would the test fail if the user-visible behavior broke?
- Does the test avoid overfitting to private implementation?
- Did you run the focused test or explain why not?

