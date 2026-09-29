# ADR 0001: Server-first system profile

- Status: Accepted
- Date: 2026-09-28

## Context

CablerOS has long-term development, gaming, and Windows-application goals, but
its first complete operating profile needs a clear priority. Designing around a
desktop first would introduce graphics and interactive policy before the kernel
has proven isolation, observability, recovery, and predictable resource use.

## Decision

CablerOS will be server-first. Early milestones will operate headlessly and
prioritize remote administration, service isolation, structured diagnostics,
safe updates, networking, storage, and measurable tail latency.

Desktop and gaming environments will be later profiles using stable native
interfaces. They will not place graphical or Windows-compatibility policy in
the kernel.

## Evidence

This decision records the project owner's stated requirement on 2026-09-28.
Performance goals will be validated using the comparison contract in
`docs/BENCHMARKS.md` rather than assumed from architectural preference.

## Consequences

- Early testing must work without a graphical display.
- Serial output remains a required bootstrap diagnostic path.
- Observability and recovery are architecture requirements, not later add-ons.
- Audio, accelerated graphics, and Windows application compatibility are
  intentionally deferred.
- Server-first does not remove the long-term desktop and gaming goals.

## Alternatives considered

A desktop-first profile was rejected for the initial milestones because it
would make hardware graphics and local interaction prerequisites for validating
core kernel behavior.
