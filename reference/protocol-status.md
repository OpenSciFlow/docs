# Protocol status matrix

OpenSciFlow is an early public draft. This page separates current evidence from planned work.

## Status summary

| Artifact | Repository | Current evidence | Current status |
|---|---|---|---|
| Plugin manifest schema | `plugin-manifest` | JSON Schema, 7 example manifests, license/citation checks, CI validation | Draft v0.1, reviewable metadata |
| Command-template rules | `plugin-manifest` | Placeholder validation, `{run_directory}` support, normalized scheduler fields, disallowed shell-fragment checks, rendering fixtures | Draft v0.1 guardrail |
| Readiness and validation levels | `plugin-manifest` | R0-R6 readiness levels, V1-V7 validation levels | Draft evidence classification scheme |
| Local-agent contract | `plugin-manifest` | Agent responsibilities and refusal rules | Draft execution contract |
| HPC/Slurm metadata | `plugin-manifest` | Portable Slurm field guide, submit-command fixture, and reviewed-wrapper metadata | Draft review guide |
| OpenSciFlow Skill | `opensciflow-skill` | Skill spec, schemas, prompts, five examples, GROMACS and MACE Slurm execution requests, Slurm workflow/execution alignment checks, BioPilot run-record crosswalk, coding-agent behavior review, validation scripts, refusal tests | Early agent-adoption draft |
| Workflow template schema | `workflow-templates` | JSON Schema, 7 protein/materials templates, CI validation, protein-template review matrix | Draft v0.1 task templates |
| Workflow DAG validation | `workflow-templates` | Step/DAG consistency checks | Draft structural validation |
| Workflow artifact handoff | `workflow-templates` | `consumes` / `produces` checks across 7 protein/materials templates | Draft executable-structure validation |
| Workflow reproducibility policy | `workflow-templates` | Validator checks input hashes, tool versions, commands, environment, report template, example-data status/license, and limitations | Draft run-record readiness guardrail |
| Run record schema | `biopilot-prototype` | JSON Schema, sample run record, CI validation | Draft reproducibility record |
| BioPilot prototype | `biopilot-prototype` | MVP runbook, API draft, demo request schema, plan-response schema, artifact-resolution schema, read-only manifest/workflow loader, sample-data policy, sample-data metadata template, protocol compliance plan | Prototype plan with validated request, blocked planning fixture, and resolved protocol-artifact summary |
| Landscape map | `awesome-ai4s-workflows` | 83 related projects, 83 assessment records, CI validation | Correction-friendly map |
| Position paper | `whitepaper` | position note and draft text | Framing draft |

## What has CI today

| Repository | CI check | Validates |
|---|---|---|
| `plugin-manifest` | Validate plugin manifests | Schema, command placeholders, command-template guardrails, license/citation metadata, Slurm submit-command rendering fixtures |
| `opensciflow-skill` | Validate skill fixtures | Skill input/output schemas, execution requests, reviewed-wrapper refusal cases, run-record schema, BioPilot run-record crosswalk |
| `workflow-templates` | Validate workflow templates | Schema, DAG consistency, plugin list structure, artifact handoff |
| `biopilot-prototype` | Validate demo request, plan response, and run records | Demo request schema, blocked planning response schema, and run-record schema against sample JSON |
| `awesome-ai4s-workflows` | Validate landscape data | Project fields, assessment fields, duplicate names, project-assessment alignment |

## What is not ready yet

- No manifest should be treated as a stable standard.
- No plugin is certified for scientific correctness.
- `mdanalysis-trajectory-analysis` is not yet `R3`; one failed local dry-run attempt is recorded, and passing dry-run evidence is still missing.
- BioPilot has not yet executed the full protein MD stability workflow.
- Sample data is still a candidate until license, citation, size, and hashes are recorded with the metadata template.

## Next evidence targets

1. Record MDAnalysis dry-run evidence and move the manifest toward `R3`.
2. Confirm sample-data provenance and hashes.
3. Produce one validated BioPilot `run_manifest.json` from a public sample run.
4. Stress-test artifact handoff checks against optional branches and fallback tools.
5. Review the second Slurm reviewed-wrapper example outside GROMACS against real materials/HPC practice.
6. Draft v0.2 command-template and run-record RFC.

## Planning references

- v0.2 RFC outline: `reference/v0.2-rfc-outline.md`
- Reviewed-wrapper RFC draft: `reference/v0.2-reviewed-wrapper-rfc.md`
- R3 evidence template: https://github.com/OpenSciFlow/plugin-manifest/blob/main/docs/r3-evidence-template.md
- Validation levels: https://github.com/OpenSciFlow/plugin-manifest/blob/main/docs/validation-levels.md
- HPC/Slurm metadata guide: https://github.com/OpenSciFlow/plugin-manifest/blob/main/docs/hpc-slurm-metadata.md
- OpenSciFlow Skill: https://github.com/OpenSciFlow/opensciflow-skill
- Skill schema mapping: https://github.com/OpenSciFlow/opensciflow-skill/blob/main/docs/schema-mapping.md
- Skill run-record alignment: https://github.com/OpenSciFlow/opensciflow-skill/blob/main/docs/run-record-alignment.md
- Skill coding-agent behavior review: https://github.com/OpenSciFlow/opensciflow-skill/blob/main/docs/coding-agent-behavior-review.md
- Skill Slurm workflow alignment: https://github.com/OpenSciFlow/opensciflow-skill/blob/main/docs/slurm-workflow-alignment.md
- Reviewed-wrapper checklist: https://github.com/OpenSciFlow/opensciflow-skill/blob/main/docs/wrapper-review-checklist.md
- Artifact handoff validation: https://github.com/OpenSciFlow/workflow-templates/blob/main/docs/artifact-handoff-validation.md
- Workflow reproducibility validation: https://github.com/OpenSciFlow/workflow-templates/blob/main/docs/reproducibility-validation.md
- Protein template review matrix: https://github.com/OpenSciFlow/workflow-templates/blob/main/docs/protein-template-review-matrix.md
- BioPilot compliance plan: https://github.com/OpenSciFlow/biopilot-prototype/blob/main/docs/protocol-compliance-plan.md
- BioPilot minimal runner contract: https://github.com/OpenSciFlow/biopilot-prototype/blob/main/docs/minimal-runner-contract.md
- BioPilot manifest/workflow loading: https://github.com/OpenSciFlow/biopilot-prototype/blob/main/docs/manifest-workflow-loading.md
- BioPilot Skill projection note: https://github.com/OpenSciFlow/biopilot-prototype/blob/main/docs/skill-run-record-projection.md
