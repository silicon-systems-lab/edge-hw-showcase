# Edge Hardware Showcase

Deterministic systems laboratory exploring **hardware–software interaction** across modern compute platforms.

Part of the **Silicon Systems Lab**.

The project focuses on understanding how software workloads interact with:

- CPU microarchitecture
- memory hierarchy
- kernel boundaries
- accelerator infrastructure

Rather than demonstrating edge AI applications, the lab investigates **systems behavior under controlled workloads**.

---

## Objectives

The primary goals of this laboratory are:

- reproducible systems experimentation
- cross-silicon performance comparison
- understanding hardware-driven performance limits
- developing silicon-aware infrastructure practices

The project intentionally prioritizes **measurement and reasoning** over application functionality.

---

## Hardware Platforms

Experiments are executed across multiple compute architectures:

- Apple Silicon hosts
- ARM SBC platforms (e.g., RK3588 class devices)
- x86 hosts

This allows comparison of memory behavior, concurrency effects, and runtime characteristics across different silicon implementations.

---

## Experiment Domains

Current experiment categories include:

```

memory/
concurrency/
kernel/
accelerator/

```

Example topics:

- sequential vs random memory access
- pointer-chasing workloads
- cache-line contention
- syscall overhead
- host–accelerator interaction

Each experiment is designed to expose specific **hardware effects**.

---

## Methodology

Experiments follow a structured engineering process:

1. Define workload hypothesis  
2. Execute deterministic workload  
3. Collect hardware performance counters  
4. Compare results across platforms  
5. Analyze root causes  

Measurement tools may include:

- Linux performance counters
- low-level profiling
- latency and throughput measurement

---

## Repository Structure

```

edge-hw-showcase
│
├─ benchmarks/
├─ analysis/
├─ device-profiles/
├─ docs/
│   └─ governance/

```

Where:

- **benchmarks** contain controlled workloads
- **analysis** contains experiment interpretations
- **device-profiles** contain hardware-specific configurations
- **docs/governance** defines laboratory policies

---

## Relationship to Silicon Systems Lab

This repository represents the **public experimental layer** of the Silicon Systems Lab.

Deeper research notes, experimental planning, and internal analysis are maintained in private repositories within the organization.

---

## Status

Early-stage laboratory infrastructure.

Initial focus is establishing deterministic measurement environments before expanding experiment coverage.
