# Communication Channels

To avoid information fragmentation, OcteDigital standardizes how engineering decisions, discussions, and tasks are recorded.

## 1. Issue

- **Purpose**: Actionable work tracking.
- **When to use**: To report a bug, request a feature, or track a specific engineering task.
- **Rule**: If it requires a code change, it needs an Issue.

## 2. Pull Request (PR)

- **Purpose**: Code review and integration.
- **When to use**: Whenever you have code ready (or in a draft state) to merge.
- **Rule**: Every PR must link to a corresponding Issue.

## 3. Discussion (GitHub Discussions / Team Chat)

- **Purpose**: Open-ended questions, brainstorming, and Q&A.
- **When to use**: When you need help debugging, want to propose a loose idea, or need architectural advice before opening an Issue or PR.
- **Rule**: Do not track actionable work in Discussions. Once a decision is made, convert it to an Issue.

## 4. ADR (Architectural Decision Record)

- **Purpose**: A historical log of significant architectural choices.
- **When to use**: When deciding on a new framework, database, or major system design change.
- **Rule**: ADRs live alongside the code in the `docs/architecture/adr/` directory.

## 5. RFC (Request for Comments)

- **Purpose**: Formal proposals for organization-wide changes.
- **When to use**: When proposing a new engineering standard, cross-team API change, or major infrastructure shift.
- **Rule**: RFCs are usually drafted as a PR modifying a design document, allowing asynchronous review from multiple teams before implementation.
