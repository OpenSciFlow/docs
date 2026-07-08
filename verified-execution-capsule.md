# Verified Execution Capsule

A verified execution capsule is a structured package of evidence around one scientific tool task.

It is not a claim that the tool runs everywhere. It records what the tool needs, what was checked, what was run, where it passed or failed, and what remains unknown.

## Capsule Contents

A capsule should include:

| Component | Purpose |
|---|---|
| Manifest | Describes inputs, outputs, environment, hardware, model weights, license, citation, safety notes, and limitations. |
| Environment spec | Describes Conda, lockfile, Docker, Apptainer, system packages, or HPC module requirements. |
| Command templates | Provides reviewed commands or reviewed wrappers. Agents must not invent shell commands. |
| Smoke tests | Defines the smallest checks, such as version checks, import checks, or tiny-input runs. |
| Test inputs | Provides minimal public or regenerable inputs for validation. |
| Expected outputs | Lists expected files or output patterns for smoke tests and example runs. |
| Run records | Stores real execution records with commands, versions, hashes, logs, return codes, artifacts, citations, and limitations. |
| Verified environment matrix | Records where the capsule passed, failed, or remains untested. |
| Known failures | Records known failure modes such as CUDA mismatch, missing weights, missing Slurm module, or permission errors. |

## Capsule Boundary

A capsule is narrower than a project.

For example, a `gromacs-rmsd` capsule may describe one RMSD analysis path with a reviewed command template and a tiny test trajectory. It should not claim to cover all GROMACS simulations, all force fields, all clusters, or all MD analysis tasks.

## Evidence Rule

The capsule should separate draft metadata from verified evidence:

- A manifest can exist before execution.
- A smoke test must have a recorded environment and result.
- An example run must have a run record.
- Multi-environment value requires a verified environment matrix.
- External reproduction requires a record from another user or machine.

## Agent Rule

An agent may inspect a capsule and prepare a plan.

It may execute only reviewed command templates or reviewed wrapper submissions declared in the capsule, after checking metadata, known failures, environment readiness, and user approval requirements.

It must not claim reproducibility beyond the verified environment matrix.
