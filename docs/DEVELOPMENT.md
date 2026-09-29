# CablerOS Development Model

CablerOS is currently developed as a private-source operating-system project.

This public repository documents the project, its architecture, roadmap,
policies, and eventually its public APIs and release/download information. It
is not the authoritative source-code repository and is not intended to provide
a public build-from-source workflow.

## Source development

The authoritative CablerOS source code and internal development tooling are
maintained on CablerOS-controlled systems.

At the current stage, development may occur on the Head Founder's approved
development system. The long-term plan is to move authoritative development to
CablerOS-controlled server infrastructure.

Approved developers or contributors must follow the
[Developer Access & Source Security Policy](legal/DEVELOPER-ACCESS.md).

## Development access

Access to private CablerOS source is not granted automatically.

A developer or contributor must:

1. be individually approved by the CablerOS Project;
2. use an individually assigned account;
3. accept the applicable CablerOS License and project policies; and
4. use CablerOS-approved systems, access methods, and development tools.

Organizations may nominate developers, but each person must still be approved
individually.

## Remote development

Remote access may be permitted when specifically approved by CablerOS and when
the required security controls are in place.

Private source is intended to remain on CablerOS-controlled infrastructure
rather than being copied to personal developer systems.

## Build and test discipline

CablerOS uses an internal build-and-test workflow for bootstrap development.

Development changes that can affect boot behavior are expected to be built,
tested, and validated in the approved CablerOS development environment before
they are treated as working.

The current bootstrap target is x86-64 UEFI and is tested in QEMU. Public
documentation may report observable milestones and test results without
publishing the private implementation or internal build scripts.

## Current implementation boundary

A bootable UEFI diagnostic exists and can enter CablerOS code and produce
diagnostic output.

This does **not** mean a complete kernel exists. Major operating-system
subsystems such as full memory management, interrupts, scheduling, drivers,
storage, networking, and system services remain development milestones unless
the roadmap or later public status documentation says otherwise.

## Public repository boundary

The public repository may contain:

- architecture and roadmap documentation;
- architecture decision records;
- legal and security policies;
- public API documentation;
- public release notes;
- official download links when releases exist; and
- other non-private project documentation.

Private implementation files, internal build scripts, local development
configuration, and private source code remain outside the public repository.
