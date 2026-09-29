# CablerOS Roadmap

The roadmap uses capability milestones instead of calendar promises.

## M0: Architecture and toolchain

- repository and build conventions
- architecture decision record template
- reproducible cross-toolchain configuration
- emulator-based test workflow
- headless serial logging and panic conventions

Exit condition: a documented build can produce and launch a minimal image in a
virtual machine, with automated verification of its first diagnostic message.

## M1: Kernel bootstrap

- UEFI handoff
- CPU initialization
- exception and interrupt handling
- physical and virtual memory managers
- deterministic panic reports

Exit condition: memory and exception self-tests pass in the emulator.

## M2: Execution

- kernel threads and scheduler
- user mode and address-space isolation
- processes, handles, and initial system calls
- IPC prototype

Exit condition: isolated user programs can run concurrently and communicate
without direct access to each other's memory.

## M3: Storage and files

- PCI discovery and one virtual block-device driver
- block cache and VFS
- bootstrap/recovery filesystem support
- CablerFS design and experimental implementation

Exit condition: data survives reboot and injected interruption tests without
silent corruption.

## M4: Native server environment

- service manager
- native runtime and command environment
- package and update prototype
- remote administration and structured observability
- basic framebuffer diagnostics

Exit condition: the system can install, supervise, observe, and remotely manage
a native CablerOS service.

## M5: Modern server hardware foundation

- multicore scheduling
- networking and common server storage
- IOMMU and interrupt scaling
- power and thermal management
- USB for recovery and administration

Exit condition: supported reference hardware can perform development tasks
without relying on firmware-only devices.

## M6: Desktop, gaming, and compatibility research

- local input, audio, and accelerated graphics
- PE loader
- selected user-space Windows API compatibility
- graphics and input translation experiments
- per-application compatibility tests

Exit condition: explicitly selected test applications run reproducibly. Broad
Windows gaming compatibility is not implied by this milestone.

