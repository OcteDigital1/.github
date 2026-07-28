# Architectural Decision Records (ADRs)

At OcteDigital, we use Architectural Decision Records (ADRs) to document significant decisions related to software architecture.

## Why use ADRs?

ADRs provide context. When engineers look at a codebase years later, they often wonder "Why was it built this way?" ADRs capture the problem, the options considered, and the justification for the final choice.

## Where do ADRs live?

ADRs should live directly within the repository they apply to, typically in a `docs/adr/` directory. For overarching organizational decisions, they may live in this `.github` repository.

## How to write an ADR

1. Copy the [ADR Template](adr-template.md).
2. Name the file sequentially (e.g., `0001-use-postgres-for-user-data.md`).
3. Fill out the sections clearly.
4. Submit a Pull Request to review the decision with the team.
