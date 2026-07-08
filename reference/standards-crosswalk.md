# Standards Crosswalk

OpenSciFlow should be positioned as an agent-safe execution evidence layer, not a competing workflow engine or metadata standard.

## Core Position

OpenSciFlow adds value when an AI agent needs to decide:

- what must be checked before running a scientific tool;
- which reviewed command template may be rendered;
- which environment has evidence;
- which known failures apply;
- what run record must be written after execution starts.

It should interoperate with existing standards rather than replace them.

## Crosswalk

| Existing standard or system | Existing role | OpenSciFlow role |
|---|---|---|
| Common Workflow Language | Portable command-line tool and workflow descriptions. | Map reviewed command templates and declared inputs/outputs to CWL concepts when useful. |
| RO-Crate | Packaging research data and metadata. | Package capsule metadata and evidence in RO-Crate-compatible form where practical. |
| Workflow Run RO-Crate | Recording workflow execution provenance. | Map OpenSciFlow run records to workflow-run provenance fields. |
| Nextflow / Snakemake | Workflow execution, scheduling, scaling, and pipeline composition. | Provide pre-execution checks and post-execution records for tools used inside workflows. |
| MCP | Connecting AI applications to tools and data sources. | Expose capsule inspection, smoke test, and reviewed execution actions as agent tools with fail-closed rules. |

## What To Avoid

- Do not present OpenSciFlow as a replacement for CWL, Nextflow, Snakemake, RO-Crate, WorkflowHub, or MCP.
- Do not create broad schema work before at least one capsule has stable R5 evidence.
- Do not imply portability beyond the verified environment matrix.
- Do not treat run records as scientific truth validation.

## Immediate Direction

The next phase should focus on a small number of R5/R6 capsules.

Priority:

1. Stabilize `mdanalysis-rmsd` as a compact R5 example.
2. Move `gromacs-rmsd` from R3 skeleton toward R4 smoke-test evidence.
3. Add crosswalk exports only after the capsule evidence is stable.
