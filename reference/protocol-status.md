# Protocol status matrix

OpenSciFlow is an early public draft. This page separates current evidence from planned work.

## Status summary

| Artifact | Repository | Current evidence | Current status |
|---|---|---|---|
| Verified execution capsule registry | `verified-capsules` | One MDAnalysis RMSD R5 capsule with tiny example outputs and run records from local venv and local Conda environments; one GROMACS RMSD R3 skeleton with a blocked local readiness record; capsule schemas, environment-spec schema, run-record schema, verified-env schema, known-failure schema | Local R5 evidence exists; no R6 cross-environment claim yet |
| Plugin manifest schema | `plugin-manifest` | JSON Schema, 7 example manifests, license/citation checks, CI validation | Draft v0.1, reviewable metadata |
| Command-template rules | `plugin-manifest` | Placeholder validation, `{run_directory}` support, normalized scheduler fields, reviewed-wrapper metadata validation, disallowed shell-fragment checks, rendering fixtures | Draft v0.1 guardrail |
| Readiness and validation levels | `plugin-manifest` | R0-R7 readiness levels, V1-V7 validation levels | Draft evidence classification scheme |
| Local-agent contract | `plugin-manifest` | Agent responsibilities and refusal rules | Draft execution contract |
| HPC/Slurm metadata | `plugin-manifest` | Portable Slurm field guide, submit-command fixture, and reviewed-wrapper metadata | Draft review guide |
| OpenSciFlow Skill | `opensciflow-skill` | Skill spec, schemas, prompts, five examples, GROMACS and MACE Slurm execution requests, Slurm workflow/execution alignment checks, BioPilot run-record crosswalk, coding-agent behavior review, validation scripts, refusal tests | Early capsule-inspection and agent-adoption draft |
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
| `verified-capsules` | Validate capsule skeletons and recorded examples | Capsule structure, manifest, environment spec, command templates, smoke-test metadata, run-record schema, verified-env matrix, known-failure records |
| `plugin-manifest` | Validate plugin manifests | Schema, command placeholders, command-template guardrails, license/citation metadata, Slurm submit-command rendering fixtures |
| `opensciflow-skill` | Validate skill fixtures | Skill input/output schemas, execution requests, reviewed-wrapper refusal cases, run-record schema, BioPilot run-record crosswalk |
| `workflow-templates` | Validate workflow templates | Schema, DAG consistency, plugin list structure, artifact handoff |
| `biopilot-prototype` | Validate demo request, plan response, and run records | Demo request schema, blocked planning response schema, and run-record schema against sample JSON |
| `awesome-ai4s-workflows` | Validate landscape data | Project fields, assessment fields, duplicate names, project-assessment alignment |

## What is not ready yet

- No manifest should be treated as a stable standard.
- No plugin is certified for scientific correctness.
- No capsule should be described as portable beyond its verified environment matrix.
- `mdanalysis-rmsd` is R5 only for the recorded tiny local Windows/Python/MDAnalysis examples; local venv plus local Conda evidence is still not R6.
- `gromacs-rmsd` has a blocked local readiness record because `gmx` is not available on PATH; it is still not R4.
- `mdanalysis-trajectory-analysis` still needs updated evidence under the R0-R7 readiness model.
- BioPilot has not yet executed the full protein MD stability workflow.
- Sample data is still a candidate until license, citation, size, and hashes are recorded with the metadata template.

## Next evidence targets

1. Stabilize `mdanalysis-rmsd` as the first compact R5 capsule.
2. Re-run `mdanalysis-rmsd` on Linux/Conda or container and move it toward `R6` only if evidence passes.
3. Install or containerize GROMACS and move the GROMACS RMSD capsule toward `R4` only after `gmx --version` passes.
4. Confirm sample-data provenance, license, citation, size, and hashes for future capsules.
5. Add standards crosswalk exports only after capsule evidence is stable.
6. Review one Slurm reviewed-wrapper example against real HPC practice.
7. Draft v0.2 capsule, command-template, verified-env, and run-record RFC.

## Planning references

- v0.2 RFC outline: `reference/v0.2-rfc-outline.md`
- Verified capsules: https://github.com/OpenSciFlow/verified-capsules
- Standards crosswalk: `reference/standards-crosswalk.md`
- Reviewed-wrapper RFC draft: `reference/v0.2-reviewed-wrapper-rfc.md`
- R3 evidence template: https://github.com/OpenSciFlow/plugin-manifest/blob/main/docs/r3-evidence-template.md
- Validation levels: https://github.com/OpenSciFlow/plugin-manifest/blob/main/docs/validation-levels.md
- HPC/Slurm metadata guide: https://github.com/OpenSciFlow/plugin-manifest/blob/main/docs/hpc-slurm-metadata.md
- Reviewed-wrapper field rules: https://github.com/OpenSciFlow/plugin-manifest/blob/main/docs/reviewed-wrapper-fields.md
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
