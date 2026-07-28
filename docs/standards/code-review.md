# Code Review Guidelines

Code reviews are a critical part of our engineering process at OcteDigital. They ensure quality, share knowledge, and prevent bugs.

## For the Author

- **Keep it small**: Smaller PRs are reviewed faster and more thoroughly. Aim for < 400 lines of code changed.
- **Self-review first**: Read your own diff before requesting a review.
- **Provide context**: Fill out the [Pull Request Template](../../PULL_REQUEST_TEMPLATE.md) completely.
- **Be responsive**: Address feedback promptly.

## For the Reviewer

- **Be respectful**: Frame feedback collaboratively.
- **Focus on architecture and logic**: Let automated tools (linters) handle style debates. Uphold our [Engineering Philosophy](../engineering-philosophy.md).
- **Use labels**: Use prefixes like `Nit:` for non-blocking minor suggestions.

## The Process

1. A PR requires at least one approval from a designated Code Owner (see [Repository Ownership](../organization/repository-ownership.md)).
2. If automated CI checks are configured for the repository, they must pass.
3. Once approved, the PR can be merged into `develop` (or `main` for hotfixes).
