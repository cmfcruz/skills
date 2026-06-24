# Foundational Agent Skills

This repo defines small, trigger-based skills for keeping code clean, readable,
and maintainable. The skills are organized around three development phases, but
the files are split by trigger so agents can load only the relevant procedure.

## Core Philosophy

Code should be easy for a human to read, change, review, and delete. These
skills exist to make agents slow down at the moments where maintainability
usually gets lost: before they understand the existing code, while they are
authoring new logic, and when they are about to call the work done.

The skills should stay:

- Procedural enough for non-frontier models to follow.
- Small enough to route cleanly.
- Explicit about when not to apply a rule.
- Focused on readable, maintainable code over clever code.
- Authored by us and evolved through use.

## Organization

Phases organize the philosophy. Triggers organize the files.

## V1 Skills

### Before Writing

- `explore-before-edit`: inspect the codebase before adding or changing code.
- `refactor-safely`: map blast radius and pin behavior before changing existing
  code.

These skills protect context. They keep agents from inventing patterns,
duplicating helpers, or refactoring behavior they have not pinned down.

### During Writing

- `house-style`: keep names, control flow, functions, and reuse clean while
  authoring code.
- `handle-failures`: write explicit, useful error paths.
- `vet-dependency`: check existing project options before adding dependencies.
- `write-tests`: test real behavior rather than implementation trivia.

These skills shape the code as it is produced. They keep implementation boring,
readable, local to the task, and aligned with the project.

### Finishing

- `finish-up`: review the diff, delete dead code, run checks, and verify claims.
- `conventional-commits`: create small commits with conventional messages.

These skills close the loop. They keep finished work reviewable, verified, and
easy to understand later.

## Skill Inventory

### `explore-before-edit`

Use before writing or changing code in an unfamiliar area. The agent should read
nearby files, search for existing helpers and patterns, and identify the local
style before editing.

### `refactor-safely`

Use before changing existing behavior, moving code, extracting helpers, or
renaming shared symbols. The agent should map callers, pin current behavior, and
avoid broad cleanup during unrelated work.

### `house-style`

Use while authoring code. This is the core readability skill: intention-revealing
names, clear control flow, small focused functions, and justified reuse without
premature abstraction.

### `handle-failures`

Use when writing error paths, validation branches, retries, fallbacks, or catch
blocks. The agent should make failures explicit, actionable, and consistent with
the surrounding code.

### `vet-dependency`

Use before adding a new dependency, package, framework, service dependency, or
uncommon import. The agent should prefer existing project tools and justify any
new dependency.

### `write-tests`

Use when adding, changing, or repairing tests. The agent should test real
behavior, avoid overfitting to implementation details, and use mocks only at
appropriate boundaries.

### `finish-up`

Use when the agent believes implementation is complete. The agent should review
the diff, remove dead code, check for accidental duplication, run focused
verification, and report what was checked.

### `conventional-commits`

Use when preparing commits. The agent should create small, scoped commits with
accurate conventional messages such as `feat:`, `fix:`, `refactor:`, `test:`,
and `docs:`.

## Skill Shape

Each skill lives in `skills/<skill-name>/SKILL.md`. The `description` frontmatter
is the routing surface, so it must include the phase and concrete trigger. Keep
skill bodies short, procedural, and explicit about when not to use the skill.
