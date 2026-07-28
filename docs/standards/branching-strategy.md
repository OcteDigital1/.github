# Branching Strategy

This document defines how we manage Git branches across all OcteDigital repositories.

## Why does this exist?

A strictly enforced branching strategy prevents merge conflicts, stabilizes releases, and provides a clear audit trail.

## The Model: GitFlow Variant

We do **NOT** use GitHub Flow (trunk-based development directly on main). Instead, we utilize a robust branching model with isolated feature and release tracks.

### The Long-Lived Branches

1. **`main`**
   - The `main` branch represents the stable production state.
   - It only accepts merges from `release/*` branches or `hotfix/*` branches.
   - Every commit on `main` is a production release and is tagged with a [Semantic Version](semantic-versioning.md).

2. **`develop`**
   - The `develop` branch serves as the integration branch for all new features.
   - It represents the latest delivered development changes for the next release.
   - Features merge into `develop`.

### The Short-Lived Branches

3. **`feature/<feature-name>`**
   - **Created from:** `develop`
   - **Merges back into:** `develop`
   - **Purpose:** Developing new features or non-emergency bug fixes for an upcoming release.

4. **`release/<version>`** (e.g., `release/1.2.0`)
   - **Created from:** `develop`
   - **Merges back into:** `main` **AND** `develop`
   - **Purpose:** Preparing a new production release. Code freeze is applied here; only bug fixes, documentation, and release-related tasks are allowed on this branch.

5. **`hotfix/<version>`** (e.g., `hotfix/1.2.1`)
   - **Created from:** `main`
   - **Merges back into:** `main` **AND** `develop`
   - **Purpose:** Emergency fixes for production issues. This allows us to patch production without waiting for the next full release cycle on `develop`.

## Workflow Example (Feature Development)

1. `git checkout develop`
2. `git pull origin develop`
3. `git checkout -b feature/user-authentication`
4. Make changes, use [Conventional Commits](commit-convention.md).
5. Open PR against `develop`.
6. Once approved, merge into `develop`.

## Workflow Example (Hotfix)

1. `git checkout main`
2. `git pull origin main`
3. `git checkout -b hotfix/1.2.1`
4. Fix the critical production bug.
5. Open PR against `main`.
6. Merge into `main` (and deploy/tag), then **immediately merge the hotfix back into `develop`** to prevent regressions.
