# Review checklists

These are the current review entry points for OpenSciFlow contributors.

## Plugin manifests

- Manifest review checklist: https://github.com/OpenSciFlow/plugin-manifest/blob/main/docs/manifest-review-checklist.md
- Readiness levels: https://github.com/OpenSciFlow/plugin-manifest/blob/main/docs/readiness-levels.md
- Protocol change process: https://github.com/OpenSciFlow/plugin-manifest/blob/main/docs/protocol-change-process.md
- Local agent contract: https://github.com/OpenSciFlow/plugin-manifest/blob/main/docs/agent-contract.md

Use these when reviewing `opensciflow.yaml` files.

## Workflow templates

- Workflow review checklist: https://github.com/OpenSciFlow/workflow-templates/blob/main/docs/workflow-review-checklist.md
- Report template convention: https://github.com/OpenSciFlow/workflow-templates/blob/main/docs/report-template-convention.md
- Example dataset policy: https://github.com/OpenSciFlow/workflow-templates/blob/main/docs/example-dataset-policy.md

Use these when reviewing task templates, report boundaries, example datasets, and workflow reproducibility.

## Agent skill behavior

- Coding-agent behavior review: https://github.com/OpenSciFlow/opensciflow-skill/blob/main/docs/coding-agent-behavior-review.md
- Refusal policy: https://github.com/OpenSciFlow/opensciflow-skill/blob/main/docs/refusal-policy.md
- Slurm workflow alignment: https://github.com/OpenSciFlow/opensciflow-skill/blob/main/docs/slurm-workflow-alignment.md
- Wrapper review checklist: https://github.com/OpenSciFlow/opensciflow-skill/blob/main/docs/wrapper-review-checklist.md

Use these when reviewing whether an AI agent should plan, refuse, dry-run, execute, or write a run record.

## Rule of thumb

If a contribution makes execution easier, it should also make review, refusal, citation, and reproducibility clearer.

## Run records

- Run record spec: https://github.com/OpenSciFlow/biopilot-prototype/blob/main/docs/run-record-spec.md
- Run record schema: https://github.com/OpenSciFlow/biopilot-prototype/blob/main/schema/opensciflow-run-record.schema.json

Use these when reviewing whether a workflow or local agent records enough information after execution.
