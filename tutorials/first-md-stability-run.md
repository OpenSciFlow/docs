# First MD Stability Run

This tutorial describes the first planned BioPilot / OpenSciFlow reference demo.

Current status: **review-only / blocked for execution**.

The current BioPilot fixture intentionally does not execute the workflow because:

- `mdanalysis-trajectory-analysis` is recorded as `R2`, not `R3`;
- MDAnalysis dry-run evidence has not passed in the current environment;
- sample data license, citation, size, and hashes are not complete.

## Goal

Analyze an existing protein molecular dynamics trajectory and generate:

- RMSD;
- RMSF;
- radius of gyration;
- plots;
- execution logs;
- artifact list;
- reproducibility manifest;
- Markdown/HTML report.

## Inputs

Required:

- `topology.pdb` or `structure.gro`
- `trajectory.xtc` or `trajectory.dcd`

Optional:

- ligand residue name or residue id;
- project title;
- analysis config YAML.

## Workflow

The intended full workflow is:

1. User enters a natural-language task.
2. Task parser maps it to `molecular-dynamics-stability-analysis`.
3. Runner validates `demo-run-request.json`.
4. Tool registry checks MDAnalysis/GROMACS readiness.
5. Local Agent creates a run directory.
6. Analysis computes RMSD, RMSF, and radius of gyration.
7. Artifacts are collected.
8. Report generator creates `report.md` and `report.html`.
9. Run manifest records commands, environment, input hashes, output hashes, citations, and limitations.

The current review-only workflow is:

1. Validate the demo request.
2. Generate a blocked planning response.
3. Record missing readiness and sample-data requirements.
4. Stop before execution.

## Current commands

From `biopilot-prototype`:

```powershell
python scripts\validate_demo_request.py
python scripts\validate_plan_response.py
python scripts\validate_run_records.py
python scripts\plan_demo_run.py
```

These commands validate protocol fixtures and print a planning response. They do not run MDAnalysis.

## Expected artifacts

```text
runs/{run_id}/
  inputs_manifest.json
  run_manifest.json
  logs/execution.log
  metrics/rmsd.csv
  metrics/rmsf.csv
  metrics/rg.csv
  plots/rmsd.png
  plots/rmsf.png
  plots/rg.png
  report/report.md
  report/report.html
```

Current blocked planning fixture:

```text
examples/protein-md-stability/plan-response.blocked.json
```

Current planned run manifest fixture:

```text
examples/protein-md-stability/sample-run-manifest.json
```

## Scientific limitation

Trajectory stability metrics are descriptive computational analyses. They do not prove binding affinity, biological mechanism, clinical relevance, or drug efficacy.

## What Must Happen Before Execution

Before this tutorial becomes an executable demo:

- MDAnalysis dry-run evidence must pass and be committed.
- Sample data license must be recorded.
- Sample data citation must be recorded.
- File sizes and SHA256 hashes must be recorded.
- The generated run record must validate.
- The report must preserve citations and limitations.
