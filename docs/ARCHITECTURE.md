# CablerOS Architecture Charter

Status: **Draft**

This document records the initial direction. A draft item is not considered a
permanent interface until an architecture decision record accepts it.

## Product definition

CablerOS is a native, server-first operating system rather than a Linux
distribution or a customized Windows installation. The long-term system
consists of a CablerOS kernel, native system services, native applications, a
CablerOS filesystem, and optional compatibility environments.

"From scratch" means that CablerOS does not use the Linux, BSD, or Windows
kernel as its runtime foundation. It does not require inventing replacements
for every useful open standard, compiler, file format, or firmware interface.

## Initial platform

- CPU architecture: x86-64 only
- Firmware: UEFI only
- Machine model: modern PCs, initially virtual machines
- Kernel language: freestanding C++ with small architecture-specific assembly
- Kernel organization: modular monolithic kernel
- Execution model: preemptive multitasking with isolated virtual address spaces
- Primary operating mode: headless, remotely administered server

Limiting the first platform keeps early failures reproducible. Additional CPU
architectures and legacy BIOS support are out of scope until the kernel is
stable enough to justify them.

## Kernel boundaries

The kernel owns:

- CPU and interrupt management
- virtual and physical memory management
- scheduling and process isolation
- device-driver execution and hardware resource arbitration
- inter-process communication primitives
- the virtual filesystem interface
- security primitives and capability enforcement

The kernel should not contain graphical shells, package management, Windows
APIs, or general application services.

## Server-first system profile

The first complete CablerOS profile targets servers. It prioritizes:

- deterministic headless boot and recovery
- remote administration with a minimal local console
- workload isolation and least-privilege services
- structured logs, metrics, tracing, and crash evidence
- predictable tail latency under CPU, memory, storage, and network pressure
- safe unattended updates with rollback
- low idle resource use and explicit resource accounting

Desktop and gaming profiles must reuse stable kernel interfaces rather than
forcing graphical policy or consumer hardware assumptions into the kernel.

## Native application platform

CablerOS will define a stable user-space ABI only after process creation,
virtual memory, handles, and IPC have working prototypes. Bootstrap builds may
use established object and debug formats. A CablerOS-native executable/package
format can be introduced only when it solves a documented requirement.

Applications should target CablerOS APIs rather than call unstable kernel
internals directly.

## Storage

Storage development is divided into layers:

1. block-device drivers
2. buffer and cache management
3. a virtual filesystem (VFS)
4. support for a simple existing filesystem for bootstrap and recovery
5. the native CablerOS filesystem, provisionally named **CablerFS**

CablerFS must be designed around crash consistency, checksums, recovery tools,
and versioned on-disk structures. It will not be used for irreplaceable data
until corruption and power-loss testing exists.

## Graphics and gaming

Gaming is a later system profile that depends on scheduling latency, input,
audio, graphics, storage, networking, and drivers. The initial graphics path
will use a firmware framebuffer for diagnostics. Hardware-accelerated graphics
comes later and must be developed behind a stable kernel/user driver interface.

The native graphics API is undecided. Compatibility with an open graphics
standard is preferable to placing a proprietary gaming API in the kernel.

## Windows executable compatibility

Running a PE `.exe` and running a Windows application are separate problems.
The future compatibility environment may provide:

- PE image loading and relocation
- DLL loading
- a user-space implementation of selected Windows APIs
- translation of graphics, audio, input, networking, and synchronization APIs

This environment is not part of the early kernel and will not weaken native
CablerOS process isolation. Kernel-mode Windows drivers and anti-cheat systems
are not initial compatibility targets.

## Decisions still required

- exact kernel ABI and handle model
- driver isolation strategy
- IPC primitives and service discovery
- native executable and package formats
- security and identity model
- graphics and audio APIs
- CablerFS on-disk design
- supported Windows API surface
- server service lifecycle and remote-management protocols
