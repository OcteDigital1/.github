# Semantic Versioning

All OcteDigital projects, APIs, and SDKs strictly follow Semantic Versioning (SemVer) 2.0.0.

## Why does this exist?

Version numbers convey meaning. They communicate the impact of a new release to consumers and engineers, indicating whether an update is safe (a bug fix) or dangerous (a breaking change).

## Version Format: MAJOR.MINOR.PATCH

Given a version number `MAJOR.MINOR.PATCH` (e.g., `2.1.4`), you increment the:

### 1. MAJOR Version (e.g., `1.4.2` -> `2.0.0`)

Incremented when you make **incompatible API changes**.

- Example: Removing a public endpoint.
- Example: Renaming a required parameter in a library.
- Note: Triggered by a `!` or `BREAKING CHANGE` in our [Commit Convention](commit-convention.md).

### 2. MINOR Version (e.g., `2.1.4` -> `2.2.0`)

Incremented when you add **functionality in a backward-compatible manner**.

- Example: Adding a new, optional endpoint.
- Example: Adding a new method to an SDK without removing existing ones.
- Note: Triggered by a `feat:` commit.

### 3. PATCH Version (e.g., `2.1.4` -> `2.1.5`)

Incremented when you make **backward-compatible bug fixes**.

- Example: Fixing a calculation error in a function.
- Example: Resolving a memory leak.
- Note: Triggered by a `fix:` commit.

## Relationship with Releases

Our [Release Process](../processes/release-process.md) relies on these version numbers to tag commits on the `main` branch.

- A `release/x.y.0` branch typically involves a MINOR bump.
- A `hotfix/x.y.z` branch always involves a PATCH bump.
