# OpenSciFlow Docs

Documentation for the OpenSciFlow early open initiative.

OpenSciFlow is not a write-once-run-anywhere system.
It is a check-before-run and record-after-run framework for AI for Science tool execution.

## Start Here

- `verified-execution-capsule.md`: what a verified execution capsule is.
- `check-before-run-record-after-run.md`: the core execution principle.
- `trajectory-to-skill.md`: how successful run trajectories can become reusable tool skills.
- `readiness-levels.md`: R0-R7 readiness levels and what each level allows.
- `known-failures.md`: how to record failure cases without hiding them.
- `concepts/plugin.md`: what a plugin manifest is.
- `concepts/workflow-template.md`: what a workflow template is.
- `concepts/local-agent.md`: how local execution works.
- `concepts/reproducibility.md`: what each run should record.
- `tutorials/first-md-stability-run.md`: first planned reference demo.
- `reference/contribution-routes.md`: where different contributors should start.
- `reference/protocol-status.md`: current evidence and readiness matrix.
- `reference/review-checklists.md`: direct links to current review checklists.
- `zh/README.md`: Chinese documentation entry point.
- `zh/quick-check.md`: Chinese quick review checklist.

## Core Position

OpenSciFlow builds verified execution capsules for AI for Science tools.

A capsule is not just a manifest. It should eventually include:

- manifest metadata;
- environment specifications;
- reviewed command templates;
- smoke tests;
- test inputs and expected outputs;
- run records;
- verified environment matrix;
- known failure cases.

The practical goal is to make tool execution explicit, checkable, diagnosable, and recordable before claiming any portability or reproducibility.

## What This Is

- A framework for describing, checking, testing, and recording AI for Science tool execution.
- A verified execution capsule registry.
- A way to turn successful run trajectories into reusable tool skills.
- A check-before-run and record-after-run protocol.
- A safety layer for agentic scientific tool execution.

## What This Is Not

- Not a universal AI Scientist.
- Not a guarantee that tools run across all environments.
- Not a replacement for Docker, Conda, Apptainer, Slurm, Nextflow, Snakemake, workflow engines, or package managers.
- Not merely a README-to-YAML summarizer.
- Not a claim that listed projects are partners or officially affiliated.
- Not a clinical, drug-discovery, or scientific truth-validation system.

## Protocol Entry Points

- Plugin protocol roadmap: https://github.com/OpenSciFlow/plugin-manifest/blob/main/docs/protocol-roadmap.md
- Manifest field policy: https://github.com/OpenSciFlow/docs/blob/main/reference/manifest-field-policy.md
- Readiness levels: https://github.com/OpenSciFlow/docs/blob/main/readiness-levels.md
- Validation levels: https://github.com/OpenSciFlow/plugin-manifest/blob/main/docs/validation-levels.md
- Local agent contract: https://github.com/OpenSciFlow/plugin-manifest/blob/main/docs/agent-contract.md
- Reviewed-wrapper field rules: https://github.com/OpenSciFlow/plugin-manifest/blob/main/docs/reviewed-wrapper-fields.md
- OpenSciFlow Skill: https://github.com/OpenSciFlow/opensciflow-skill
- BioPilot manifest/workflow loading: https://github.com/OpenSciFlow/biopilot-prototype/blob/main/docs/manifest-workflow-loading.md
- Workflow reproducibility validation: https://github.com/OpenSciFlow/workflow-templates/blob/main/docs/reproducibility-validation.md
- Verified capsule registry: https://github.com/OpenSciFlow/verified-capsules

## BioPilot Relationship

BioPilot is the first reference prototype under the OpenSciFlow initiative.

It should not be read as a mature platform. Its role is to test whether OpenSciFlow artifacts can support a narrow local protein-computing workflow while preserving explicit checks, limitations, run records, and failure boundaries.
