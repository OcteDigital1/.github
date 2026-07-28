# Commit Convention

OcteDigital enforces the [Conventional Commits](https://www.conventionalcommits.org/) specification organization-wide.

## Why does this exist?

Standardized commit messages allow us to easily trace history, automate versioning (SemVer), and auto-generate changelogs during our [Release Process](../processes/release-process.md).

## Format

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

## Standardized Commit Types

- **`feat`**: Introduces a new feature. (Correlates with MINOR in Semantic Versioning).
- **`fix`**: Patches a bug in the codebase. (Correlates with PATCH in Semantic Versioning).
- **`docs`**: Changes to documentation only (e.g., `README.md`, inline code comments).
- **`style`**: Changes that do not affect the meaning of the code (formatting, missing semi-colons, etc).
- **`refactor`**: A code change that neither fixes a bug nor adds a feature, but improves the internal structure.
- **`perf`**: A code change that improves performance.
- **`test`**: Adding missing tests or correcting existing tests.
- **`build`**: Changes that affect the build system or external dependencies (e.g., npm, pip, go modules).
- **`ci`**: Changes to CI/CD configuration files and scripts (e.g., GitHub Actions workflows).
- **`chore`**: Maintenance tasks, routine tasks, or tooling changes that don't modify source or test files.
- **`revert`**: Reverts a previous commit.

## Breaking Changes

Any breaking change (correlating with MAJOR in Semantic Versioning) MUST be indicated by appending a `!` after the type/scope, or by including `BREAKING CHANGE:` in the footer.

## Examples

**Feature (feat)**
`feat(auth): add google SSO integration`

**Bug Fix (fix)**
`fix(ui): resolve button alignment issue on mobile`

**Refactor (refactor)**
`refactor(api): consolidate user validation logic`

**Breaking Change (feat!)**

```
feat(database)!: drop support for legacy postgres versions

BREAKING CHANGE: Postgres versions below 13 are no longer supported.
```
