# First MD Stability Run

This tutorial describes the first planned BioPilot / OpenSciFlow reference demo.

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

1. User enters a natural-language task.
2. Task parser maps it to `molecular-dynamics-stability-analysis`.
3. Tool registry checks MDAnalysis/GROMACS readiness.
4. Local Agent creates a run directory.
5. Analysis computes RMSD, RMSF, and radius of gyration.
6. Artifacts are collected.
7. Report generator creates `report.md` and `report.html`.
8. Run manifest records commands, environment, input hashes, output hashes, citations, and limitations.

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

## Scientific limitation

Trajectory stability metrics are descriptive computational analyses. They do not prove binding affinity, biological mechanism, clinical relevance, or drug efficacy.

