# OpenSciFlow Docs

User and contributor documentation for the OpenSciFlow initiative and BioPilot reference prototype.

## Start here

- `concepts/plugin.md`: what a plugin manifest is.
- `concepts/workflow-template.md`: what a workflow template is.
- `concepts/local-agent.md`: how local execution works.
- `concepts/reproducibility.md`: what each run should record.
- `tutorials/first-md-stability-run.md`: first planned reference demo.
- `reference/contribution-routes.md`: where different contributors should start.
- `reference/review-checklists.md`: direct links to current review checklists.
- `reference/roadmap.md`: near-term roadmap from draft metadata toward executable evidence.
- `reference/protocol-status.md`: current evidence and readiness matrix.
- `reference/v0.2-rfc-outline.md`: decisions needed before an executable-contract RFC.
- `reference/v0.2-reviewed-wrapper-rfc.md`: draft RFC section for Slurm and reviewed wrapper scripts.
- `reference/faq.md`: common questions.
- `reference/glossary.md`: short definitions.
- `zh/README.md`: Chinese documentation entry point.
- `zh/quick-check.md`: Chinese quick review checklist.

## Protocol and outreach entry points

- Plugin protocol roadmap: https://github.com/OpenSciFlow/plugin-manifest/blob/main/docs/protocol-roadmap.md
- Readiness levels: https://github.com/OpenSciFlow/plugin-manifest/blob/main/docs/readiness-levels.md
- Local agent contract: https://github.com/OpenSciFlow/plugin-manifest/blob/main/docs/agent-contract.md
- Manifest review checklist: https://github.com/OpenSciFlow/plugin-manifest/blob/main/docs/manifest-review-checklist.md
- License and citation policy: https://github.com/OpenSciFlow/plugin-manifest/blob/main/docs/license-and-citation.md
- OpenSciFlow Skill: https://github.com/OpenSciFlow/opensciflow-skill
- OpenSciFlow Skill schema mapping: https://github.com/OpenSciFlow/opensciflow-skill/blob/main/docs/schema-mapping.md
- OpenSciFlow Skill run-record alignment: https://github.com/OpenSciFlow/opensciflow-skill/blob/main/docs/run-record-alignment.md
- OpenSciFlow Skill wrapper review checklist: https://github.com/OpenSciFlow/opensciflow-skill/blob/main/docs/wrapper-review-checklist.md
- HPC/Slurm metadata guide: https://github.com/OpenSciFlow/plugin-manifest/blob/main/docs/hpc-slurm-metadata.md
- Workflow review checklist: https://github.com/OpenSciFlow/workflow-templates/blob/main/docs/workflow-review-checklist.md
- Run record schema: https://github.com/OpenSciFlow/biopilot-prototype/blob/main/schema/opensciflow-run-record.schema.json
- BioPilot compliance plan: https://github.com/OpenSciFlow/biopilot-prototype/blob/main/docs/protocol-compliance-plan.md
- BioPilot minimal runner contract: https://github.com/OpenSciFlow/biopilot-prototype/blob/main/docs/minimal-runner-contract.md
- Model manifest backlog: https://github.com/OpenSciFlow/plugin-manifest/blob/main/docs/model-manifest-backlog.md
- Roadmap: https://github.com/OpenSciFlow/docs/blob/main/reference/roadmap.md
- Protocol status matrix: https://github.com/OpenSciFlow/docs/blob/main/reference/protocol-status.md
- v0.2 RFC outline: https://github.com/OpenSciFlow/docs/blob/main/reference/v0.2-rfc-outline.md
- Promotion kit: https://github.com/OpenSciFlow/community/blob/main/outreach/promotion-kit.md

## What is OpenSciFlow?

OpenSciFlow is an early open initiative for modular, reproducible, local-first, and HPC-ready AI for Science workflows.

It focuses on:

- plugin manifests;
- reusable workflow templates;
- local/HPC execution patterns;
- logs, artifacts, reports, and run records;
- license, citation, and limitation metadata.

## What OpenSciFlow is not

- Not a mature ecosystem yet.
- Not a closed AI scientist platform.
- Not a replacement for established workflow engines.
- Not a clinical or drug-development decision system.
- Not a hosted GPU/model service.

## BioPilot relationship

BioPilot is the first reference prototype under the OpenSciFlow initiative. It starts with protein-computing workflows, especially molecular dynamics stability analysis.
