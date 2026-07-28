# Release Process

This document details the lifecycle of releasing software into production at OcteDigital.

## Prerequisites

Releases strictly follow our [Branching Strategy](../standards/branching-strategy.md) and [Semantic Versioning](../standards/semantic-versioning.md).

## The Lifecycle

### 1. Preparing the Release

When `develop` has accumulated enough features for the next planned release, a designated maintainer or engineering lead branches off `develop` to create a release branch:
`git checkout -b release/1.2.0 develop`

_Note: Once this branch is created, `develop` is unblocked to receive features for the subsequent release._

### 2. Stabilization

The `release/1.2.0` branch is deployed to the Staging environment.

- Only bug fixes, documentation updates, and release preparations are allowed on this branch.
- No new features are permitted.

### 3. Production Deployment (Merging)

Once the release is verified in the Staging environment:

1. The release branch is merged into `main`.
2. The merge commit on `main` is tagged with the version number (e.g., `v1.2.0`).
3. Production deployments are triggered from the tagged `main` branch, utilizing CI/CD automation where available.

### 4. Backporting

Crucially, the release branch must also be merged back into `develop` so that any bug fixes made during the stabilization phase are not lost in future releases:
`git checkout develop`
`git merge release/1.2.0`

### 5. Cleanup

The release branch is deleted from the remote repository.

## Hotfixes

For critical production issues that cannot wait for a standard release cycle:

1. Branch from `main`: `git checkout -b hotfix/1.2.1 main`
2. Fix the bug, test, and merge directly into `main` (tagging the new patch version).
3. Merge the hotfix branch back into `develop`.
