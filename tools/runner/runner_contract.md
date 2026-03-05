# Runner Contract

The runner executes any experiment directory using its `manifest.yaml`.

## Required inputs
- Experiment directory path
- A key-value map of parameters (overrides `manifest.yaml params`)

## Execution steps
1. Validate `manifest.yaml` against schema.
2. Execute `entry.run`
3. Execute `entry.measure`
4. Validate `outputs.artifact` JSON against result schema.
5. Store artifact under:
   `analysis/runs/<platform>/<experiment-id>/<timestamp>.json`

## Failure rules
- If schema validation fails: hard fail.
- If artifact missing: hard fail.
- If artifact invalid: hard fail.
- No "best effort" runs. Determinism > convenience.
