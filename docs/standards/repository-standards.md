# Repository Standards

Consistency across repositories allows engineers to jump between projects without spending hours configuring their environment.

## Baseline Requirements

Every repository MUST have:

1. **`README.md`**: Explains setup, testing, and building.
2. **`.gitignore`**: Appropriate ignores for the stack.
3. **`LICENSE`**: An appropriate license file, ensuring proprietary code is correctly protected.
4. **CI/CD Pipeline**: We strongly recommend configuring automated tests and linters to run on Pull Requests.
5. **Dependency Management**: Lock files must be committed (e.g., `package-lock.json`).
6. **CODEOWNERS**: Must map to a team defined in [Teams & Ownership](../organization/teams.md).

By default, repositories inherit the community health files (`CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`, etc.) and issue templates from this central `.github` repository.
