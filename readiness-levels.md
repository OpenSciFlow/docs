# Readiness Levels

Readiness levels describe evidence for a tool capsule.

They do not certify scientific correctness. They do not guarantee that a tool runs everywhere.

## Levels

| Level | Name | Meaning |
|---|---|---|
| R0 | Project indexed only | Only a project link and basic information exist. |
| R1 | Draft manifest | A manifest draft exists, but it has not been validated. |
| R2 | Schema-validated manifest | The manifest passes schema validation. |
| R3 | Environment spec and command templates available | Environment information and reviewed command templates exist. |
| R4 | Smoke test passed in one environment | A minimal smoke test passed in at least one recorded environment. |
| R5 | Example run passed with run record | A real example run passed in at least one environment and produced a run record. |
| R6 | Multi-environment verification | The capsule has passed or failed with records across two or more heterogeneous environments. |
| R7 | External reproduction | An external user or external machine reproduced the capsule successfully and recorded evidence. |

## What Each Level Allows

| Level | Agent may inspect? | Agent may execute? | Main warning |
|---|---|---|---|
| R0 | Yes | No | Landscape only. |
| R1 | Yes | No | Draft metadata only. |
| R2 | Yes | No by default | Schema-valid does not mean runnable. |
| R3 | Yes | Usually no beyond local readiness checks | Commands exist but no smoke-test evidence yet. |
| R4 | Yes | Smoke test with approval | Evidence applies only to the recorded environment. |
| R5 | Yes | Example run with approval | Reuse should stay within the verified environment boundary. |
| R6 | Yes | Yes with environment matching and approval | Cross-environment value is evidence-backed but still bounded. |
| R7 | Yes | Yes with environment matching and approval | External reproduction exists, but scientific correctness is still not certified. |

## Interpretation Rule

- R1/R2 may reduce documentation-understanding cost.
- R4/R5 may cautiously reduce trial-and-error cost in the verified environment.
- R6/R7 provide stronger evidence for cross-environment migration or external reproduction.

Do not say a capsule reduces execution trial-and-error cost until at least R4 evidence exists.

Do not claim cross-environment reproducibility until R6 or R7 evidence exists.

## Required Evidence

### R1

- Draft manifest exists.
- Required fields are visible, even if incomplete.

### R2

- Manifest validates against the current schema.

### R3

- Environment spec exists.
- Reviewed command templates or reviewed wrapper metadata exist.
- Required model weights, licenses, citations, and inputs are declared.

### R4

- Smoke test command exists.
- Smoke test result is recorded.
- Environment information is recorded.
- Failure or success is explicit.

### R5

- Example input exists or is regenerable.
- Expected outputs are listed.
- Example run completed.
- Run record captures commands, versions, parameters, logs, return code, artifacts, hashes, citations, licenses, limitations, and warnings.

### R6

- Two or more environments are recorded.
- Differences between environments are explicit.
- Known failures are not hidden.

### R7

- Reproduction evidence comes from an external user, machine, lab, or CI environment.
- The reproduced run record is linked or included.
