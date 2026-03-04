# Laboratory Scope

This document defines the **technical scope and boundaries** of the Edge Hardware Showcase laboratory.

The purpose of the lab is to study **hardware–software interaction under deterministic workloads** and to develop practical engineering intuition for systems running on modern silicon platforms.

---

## Core Objective

The laboratory investigates how software behavior is influenced by:

- CPU microarchitecture
- memory hierarchy
- kernel boundaries
- concurrency effects
- accelerator infrastructure

The goal is to produce **reproducible experiments** that reveal hardware-driven performance characteristics.

---

## In-Scope Domains

The following experiment domains are considered core to the laboratory.

### Memory Systems

Experiments exploring memory hierarchy behavior:

- sequential vs random memory access
- pointer chasing
- cache locality
- TLB pressure

---

### Concurrency

Workloads exposing multi-core interaction:

- false sharing
- cache line contention
- lock contention
- thread scheduling effects

---

### Kernel Interaction

Experiments focusing on kernel boundaries:

- syscall overhead
- blocking vs event-driven IO
- scheduler behavior
- kernel-user transitions

---

### Accelerator Infrastructure

Experiments related to host interaction with accelerators:

- host-to-device latency
- DMA overhead
- batching effects
- runtime orchestration patterns

Accelerator experiments may involve devices such as:

- GPUs
- NPUs
- other specialized compute accelerators

---

## Hardware Targets

The laboratory currently targets the following compute platforms:

- Apple Silicon hosts
- ARM single-board computers
- x86 systems

Experiments are designed to allow **cross-silicon comparison** whenever possible.

---

## Experiment Design Principles

All experiments should follow these principles:

### Determinism

Workloads must run under controlled conditions.

Examples:

- fixed CPU governor
- stable thermal conditions
- repeatable runtime environment

---

### Measurement First

Experiments must collect objective data before conclusions are drawn.

Typical measurements include:

- latency
- throughput
- hardware performance counters

---

### Minimal Workloads

Experiments should isolate a **single hardware effect** whenever possible.

Large application benchmarks are discouraged unless they help expose a specific systems phenomenon.

---

## Out-of-Scope Topics

The following areas are intentionally excluded from this laboratory.

### Cloud Infrastructure

Topics such as:

- Kubernetes orchestration
- Terraform automation
- cloud platform configuration

are outside the scope of this repository.

---

### Application-Level Edge AI

The laboratory does not focus on:

- computer vision demos
- model accuracy evaluation
- application-level AI pipelines

Such systems may appear only when needed to expose underlying hardware behavior.

---

### Silicon Design

This laboratory does not cover:

- RTL design
- chip layout
- EDA tooling

The focus remains on **systems running on silicon**, not silicon development itself.

---

## Relationship to Internal Research

This repository represents the **public experimental layer** of the laboratory.

Internal research materials such as:

- detailed experiment planning
- deeper performance analysis
- interview preparation notes

may be maintained in private repositories.

---

## Expected Outcomes

The laboratory aims to produce:

- reproducible performance experiments
- cross-platform comparisons
- documented systems reasoning
- infrastructure insights relevant to modern compute platforms
