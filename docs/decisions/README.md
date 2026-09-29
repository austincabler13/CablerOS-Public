# Architecture Decision Records

Architecture decision records (ADRs) preserve why an important choice was made.
They prevent the project from relying on memory or repeatedly reopening settled
questions without new evidence.

## States

- **Proposed:** under discussion; implementation must not depend on it yet
- **Accepted:** current direction
- **Superseded:** replaced by a newer ADR
- **Rejected:** considered and deliberately not selected

Copy [0000-template.md](0000-template.md) when proposing a decision. Number ADRs
sequentially and never rewrite an accepted decision to hide its history. Add a
new ADR that supersedes it instead.

## Records

- [0001: Server-first system profile](0001-server-first.md)
