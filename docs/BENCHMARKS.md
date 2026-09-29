# Performance and Feature Targets

Status: **Draft**

CablerOS aims to exceed Ubuntu on selected server workloads over the long term.
That statement is not considered true without reproducible evidence.

## Comparison contract

Every comparison must record:

- CablerOS and Ubuntu build/version identifiers
- identical physical hardware and firmware settings
- compiler and workload versions
- warm-up procedure and number of repetitions
- raw results, not only averages
- median and tail latency where applicable
- CPU, memory, storage, network, and power conditions
- all tuning applied to either system

Ubuntu must be given reasonable, documented tuning. CablerOS will not claim a
win obtained by intentionally misconfiguring its baseline.

## Initial metric groups

- boot-to-service-ready time
- idle and per-service memory footprint
- process and thread creation latency
- context-switch and IPC latency
- network throughput and p50/p95/p99 latency
- storage throughput, latency, and crash recovery
- scheduler behavior under mixed latency/throughput load
- service isolation overhead
- update rollback time and failure recovery

## Feature quality

Feature comparisons include operability, not just feature count:

- failure diagnostics are actionable
- configuration is versionable and testable
- services can be upgraded and rolled back safely
- security boundaries have explicit threat models
- administrative actions are auditable

Benchmarks will be automated when the relevant subsystem becomes functional.
