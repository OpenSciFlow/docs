# Strategic Pivot: Evidence-First Capsules

Date: 2026-07-08

## Decision

OpenSciFlow should stop optimizing for repository count, manifest count, and broad ecosystem language.

The next phase should optimize for a small number of real verified execution capsules.

## Why

The project is most credible when it shows:

- a real tool can be checked before running;
- execution uses a reviewed command template;
- a smoke test or example run actually passes;
- outputs and run records are committed;
- known failures are explicit;
- portability claims are bounded to the verified environment matrix.

Broad manifest drafts are useful, but they do not prove execution value.

## New Priority Order

1. R5 capsule evidence.
2. Known failure cases.
3. Agent refusal behavior.
4. Standards crosswalk.
5. Community correction requests.
6. New manifests or landscape expansion.

## Immediate Targets

- Keep `mdanalysis-rmsd` as the compact R5 reference.
- Move `gromacs-rmsd` from R3 skeleton to R4 smoke-test evidence.
- Attempt one second environment for `mdanalysis-rmsd` only when the environment is real and recorded.
- Add cross-standard export notes after evidence stabilizes.

## Language Boundary

Use:

- check-before-run;
- record-after-run;
- verified execution capsule;
- known failure record;
- verified environment matrix;
- bounded run record evidence.

Avoid:

- run anywhere;
- mature standard;
- universal AI Scientist;
- replacement for CWL, Nextflow, Snakemake, RO-Crate, WorkflowHub, or MCP;
- scientific correctness validation.
