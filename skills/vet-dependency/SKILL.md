---
name: vet-dependency
description: Use during writing before adding a package, library, framework, service dependency, or new import that is not already common in the repository. Do not use for dependencies explicitly required by the user.
---

# Vet Dependency

Avoid adding dependencies when the project already has a suitable solution.

## Steps

1. Search existing dependencies and imports.
2. Check whether the standard library or existing utilities are enough.
3. Prefer established project dependencies over new packages.
4. If adding a dependency is still justified, state why.
5. Update lockfiles and tests using the project-native package manager.

## Final Check

- Is the dependency necessary?
- Is it already present in the project?
- Did you avoid adding a package for trivial code?

