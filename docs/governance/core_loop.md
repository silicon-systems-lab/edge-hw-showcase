# Core Experiment Loop

All experiments in this laboratory follow a deterministic execution loop.

```
hypothesis
    ↓
experiment execution
    ↓
measurement collection
    ↓
artifact storage
    ↓
cross-platform comparison
    ↓
interpretation
```

## 1. Core Loop

```
Hypothesis → Execute → Measure → Store → Compare → Interpret
```

## 2. Experiment Contract

This repository enforces determinism via contracts:

- Experiment Manifest (what runs)
- Runner Contract (how it runs)
- Result Artifact Schema (what is produced)

No experiment is considered valid unless it produces a schema-valid artifact.

Any experiment boilerplate is:

```

experiment/
│
├─ README.md
├─ run script
├─ measurement script
└─ analysis document

```

## 3. Result Artifact Format

Results should be stored as **machine-readable artifacts**.

Example:
```
results/
  m2_max_run_01.json
  rk3588_run_01.json
```

Artifacts must include:
```
- hardware
- kernel version
- runtime configuration
- raw measurements
- timestamp
```

## 4. Baseline Policy
Baseline measurements must be stored and versioned.

Baseline changes require:
```
- commit message justification
- hardware change log
- measurement comparison
```

## 5. Escalation Rule
Performance investigation must follow this order:
```
workload
↓
runtime
↓
kernel
↓
hardware
```

Skipping layers is prohibited.

## 6. Experiment Directory Contract
