---
name: refactor-safely
description: Use before changing existing behavior, refactoring shared logic, extracting helpers from existing code, moving code, renaming public symbols, or editing code with unknown callers. For orienting in a new area before writing fresh code, use explore-before-edit instead. Do not use for brand-new isolated code.
---

# Refactor Safely

Protect existing behavior before changing structure.

## Steps

1. Find all known callers and entry points.
2. Identify behavior that must remain unchanged.
3. Locate existing tests or add characterization tests before restructuring.
4. Make the smallest behavior-preserving change.
5. Run focused tests that cover the changed behavior and callers.

## When Not To Use

Do not use this skill to justify broad cleanup during an unrelated feature. If
the cleanup is not required, leave it for a separate task.

## Final Check

- Are callers mapped?
- Is current behavior pinned by tests or explicit verification?
- Is the change behavior-preserving unless the user asked otherwise?
