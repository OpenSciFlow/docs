# Manifest field policy

OpenSciFlow v0.1 uses an explicit-field policy for plugin manifests.

If a field affects execution, licensing, citation, model-weight provenance, hardware expectations, reproducibility, or scientific interpretation, it should be present in every draft manifest.

This is why fields such as `hardware`, `model_weights`, `expected_runtime`, `safety_notes`, and `limitations` are required even when the answer is simple.

Examples:

- A non-ML tool should still say `model_weights.required: false`.
- A workflow using user-provided data should still say `license.data: "user-provided"`.
- A draft model manifest can use `checksum: "to-be-filled"`, but a local agent should treat that as a warning before execution.
- A manifest can omit `execution.slurm` unless it claims Slurm/HPC support.

The detailed protocol rule lives in the plugin-manifest repository:

```text
https://github.com/OpenSciFlow/plugin-manifest/blob/main/docs/required-vs-optional-fields.md
```

## Why this matters

The goal is not bureaucratic completeness. The goal is to stop an agent from treating an under-specified scientific tool as ready to run.

A manifest with explicit unknowns is better than a manifest that silently omits license, weight, hardware, or limitation information.
