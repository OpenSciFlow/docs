# OpenSciFlow roadmap

This roadmap is a working draft, not a promise of a mature platform.

The near-term goal is to turn the current protocol drafts into small, reviewable, executable evidence.

## Current baseline

As of 2026-07-06:

- public GitHub organization exists;
- landscape map includes 79+ related projects;
- plugin manifest schema validates 7 example manifests;
- workflow template schema validates 5 protein workflow templates;
- command-template placeholder validation and minimal rendering fixtures exist for plugin examples;
- DAG validation exists for workflow templates;
- artifact handoff validation exists for the initial protein workflow templates;
- BioPilot has a run-record schema and sample run-record validation;
- BioPilot has a sample-data metadata template, but the candidate dataset is not finalized;
- public outreach is framed as correction requests, not partnership claims.

## Next 2 weeks

Target outcome:

```text
One narrow workflow can move from metadata draft to dry-run evidence.
```

Priorities:

- Move `mdanalysis-trajectory-analysis` toward `R3 dry-run ready`.
- Convert the recorded failed MDAnalysis dry-run attempt into passing R3 evidence in a documented environment.
- Expand command-rendering fixtures for optional inputs and wrapper-script cases.
- Stress-test workflow artifact handoff checks for optional branches and fallback tools.
- Decide the first public sample trajectory and fill license, citation, size, and hash metadata.
- Use `reference/v0.2-rfc-outline.md` to keep protocol changes scoped.

## Month 1

Target outcome:

```text
BioPilot can produce a validated run record for one public sample workflow.
```

Priorities:

- Implement a minimal local runner for `Protein MD Stability Report Lite`.
- Generate `run_manifest.json` and validate it against the run-record schema.
- Produce Markdown report output with citations and limitations.
- Keep execution local-first; do not introduce hosted GPU or private-data upload.
- Document what the demo proves and what it does not prove.

## Month 2

Target outcome:

```text
The protocol can represent real local/HPC execution needs more accurately.
```

Priorities:

- Tighten Slurm/HPC metadata fields.
- Add Apptainer/container metadata conventions.
- Draft workflow-engine interoperability notes for Nextflow, Snakemake, CWL, and AiiDA.
- Add at least two more reviewed manifest drafts in different domains.
- Add one non-protein workflow-template draft only if the task boundary is narrow.

## Month 3

Target outcome:

```text
OpenSciFlow v0.2 can be proposed as an executable-contract RFC.
```

Priorities:

- Write v0.2 RFC for typed command templates, input references, output references, and run records.
- Collect external corrections from upstream maintainers and domain users.
- Separate stable fields from experimental fields.
- Decide whether BioPilot should remain a prototype repo or become a protocol compliance demo.
- Publish a short position note summarizing what changed after public correction.

## Not on the roadmap yet

- Claiming OpenSciFlow as a standard body.
- Building a closed hosted platform.
- Auto-installing arbitrary packages without user review.
- Letting an LLM generate unreviewed shell commands.
- Claiming computational outputs prove biological function, drug efficacy, clinical meaning, or materials discovery.
