# Experiment Template

Status: draft

This document defines the structure used to describe experiments
within the Edge Hardware Showcase laboratory.

Sections will include:

- experiment description
- hypothesis
- workload design
- measurement methodology
- results
- interpretation

---

# Experiment Structure Contract
- Experiment Directory Contract

All experiments in this repository must follow a consistent directory structure.

This ensures reproducibility and comparability across hardware platforms.

---

## Standard Layout
```
experiments/

    memory/
        pointer_chase/
            README.md
            run.sh
            measure.sh
            config.yaml
        results/

    concurrency/
        false_sharing/
            README.md
            run.sh
            measure.sh
            config.yaml
        results/

    kernel/
        syscall_cost/
            README.md
            run.sh
            measure.sh
            config.yaml
        results/

    accelerator/
```

---

## Required Files

Each experiment directory must contain:

### README.md

Describes:

- experiment hypothesis
- hardware configuration
- measurement method

---

### run script

Executes the workload.

Example:

```
run.sh
run.rs
run.py
```

---

### measurement script

Collects performance metrics.

Typical tools include:

- perf
- hardware counters
- latency measurement tools

---

### config file

Defines experiment parameters.

Example:
```
config.yaml
```

Parameters may include:
```
- input size
- thread count
- iteration count
- runtime flags
```


---

### results directory

Stores machine-readable artifacts.

Example:
```
results/
    m2_max_run01.json
    rk3588_run01.json
```

Artifacts must include:
```
- hardware platform
- kernel version
- runtime configuration
- raw measurements
- timestamp
```


---

## Cross-Silicon Requirement

Experiments must be runnable on multiple hardware targets.

Initial targets:

- Apple M-series
- RK3588 SBC
- x86 host systems

Each run must generate a separate artifact.

---

## Analysis Documents

Each experiment must eventually include an analysis document:
```
analysis/
    pointer_chase_analysis.md
```
