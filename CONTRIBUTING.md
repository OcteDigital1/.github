# Contributing to OcteDigital

First, thank you for contributing to OcteDigital! Whether you are an internal engineer or an external collaborator, your contributions are highly valued.

This document outlines our standard process for contributing to any OcteDigital repository.

## 1. Finding Something to Work On

- Check the repository's **Issues** tab for unassigned tasks.
- Look for issues labeled `good first issue` or `help wanted`.
- If you have an idea for a new feature or improvement, open an issue first to discuss it with the maintainers.

## 2. Setting Up Your Environment

Refer to the repository's local `README.md` for specific setup instructions. For general engineering standards and our core tenets, please read our [Engineering Philosophy](docs/engineering-philosophy.md).

## 3. Making Changes

1. **Branching**: Follow our [Branching Strategy](docs/standards/branching-strategy.md). **Always branch off `develop`** for new features and use descriptive branch names (e.g., `feature/auth-service`).
2. **Commits**: Adhere to our [Commit Convention](docs/standards/commit-convention.md). We use Conventional Commits strictly.
3. **Coding Standards**: Ensure your code follows the established standards for the repository. Run all linters, formatters, and tests before committing.

## 4. Submitting a Pull Request

1. Push your branch to GitHub.
2. Open a Pull Request against the `develop` branch (unless it is a `hotfix/`, which targets `main`).
3. The PR description will automatically populate with our [Pull Request Template](PULL_REQUEST_TEMPLATE.md). Fill it out completely.
4. Link the PR to the relevant issue(s).
5. Ensure all CI checks pass.

## 5. Code Review

All PRs require at least one approval from a designated code owner. See our [Code Review Guidelines](docs/standards/code-review.md) for expectations. Address any feedback promptly. Once approved, the PR can be merged.

## Getting Help

If you need assistance, reach out on our internal engineering channels or refer to our [Support Guidelines](SUPPORT.md).
