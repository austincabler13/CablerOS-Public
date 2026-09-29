# CablerOS

CablerOS is an experimental, modern, server-first operating system built from
scratch. Desktop development and gaming are later platform profiles built on
the same independent core.

The project is intentionally independent: it will have its own kernel, system
services, user environment, native application model, and filesystem. Existing
Windows applications are a long-term compatibility goal, not the foundation of
the system.

## Current status

- **Version:** `0.0.1-dev.0`
- **Phase:** architecture and bootstrap development
- **Target:** x86-64 PCs using UEFI

A bootable diagnostic exists; no operating-system release exists yet.

## Repository model

This repository is the **public CablerOS project repository**.

It is intended to contain public-facing material such as:

- project documentation;
- architecture and roadmap information;
- public API documentation when APIs are available;
- release notes and official download links when releases exist;
- legal, privacy, security, and service policies; and
- public project instructions and contribution information.

The CablerOS operating-system source code, internal build scripts, private
development configuration, and other implementation files are developed on
CablerOS-controlled systems and are **not published in this public repository**.

Source access for approved developers or contributors is governed by the
CablerOS License and the Developer Access & Source Security Policy.

## Engineering principles

- Design decisions are documented before they become hard dependencies.
- Correctness, debuggability, and recovery come before performance tuning.
- Hardware interfaces and public standards may be used without inheriting
  another operating system's architecture.
- Compatibility layers stay outside the kernel whenever practical.
- Every milestone must have an observable, testable completion condition.
- Performance claims require reproducible comparisons against a named baseline.

## Development model

CablerOS development currently happens in a private development environment.
Public documentation may describe the project's architecture, milestones, and
observable development status, but it is not a public source-build guide.

Approved developers work under the project's private-source access and security
rules. See [Development model](docs/DEVELOPMENT.md) for details.

## Documentation

- [Architecture](docs/ARCHITECTURE.md)
- [Roadmap](docs/ROADMAP.md)
- [Versioning](docs/VERSIONING.md)
- [Performance targets](docs/BENCHMARKS.md)
- [Development model](docs/DEVELOPMENT.md)
- [Architecture decisions](docs/decisions/README.md)

## Legal & policies

CablerOS is currently using draft legal and policy documents while the project is in development.

- [CablerOS License 1.0 — Draft](LICENSE-DRAFT.md)
- [Legal & policy index](docs/legal/README.md)
- [Developer access & source security policy](docs/legal/DEVELOPER-ACCESS.md)
- [Security & vulnerability disclosure policy](docs/legal/SECURITY.md)
- [Repository & service rules](docs/legal/SERVICES.md)
- [Privacy policy — draft outline](docs/legal/PRIVACY.md)

These documents are not yet approved for production reliance and should be
reviewed by a qualified software/IP attorney before a production release.

## Public release status

There is currently no public CablerOS operating-system download.

When an official public build becomes available, this repository may provide an
official download link and the applicable license-acceptance flow.
