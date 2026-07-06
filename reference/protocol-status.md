# Protocol status matrix

OpenSciFlow is an early public draft. This page separates current evidence from planned work.

## Status summary

| Artifact | Repository | Current evidence | Current status |
|---|---|---|---|
| Plugin manifest schema | `plugin-manifest` | JSON Schema, 7 example manifests, CI validation | Draft v0.1, reviewable metadata |
| Command-template rules | `plugin-manifest` | Placeholder validation, disallowed shell-fragment checks, rendering fixtures | Draft v0.1 guardrail |
| Readiness levels | `plugin-manifest` | R0-R6 document | Draft classification scheme |
| Local-agent contract | `plugin-manifest` | Agent responsibilities and refusal rules | Draft execution contract |
| Workflow template schema | `workflow-templates` | JSON Schema, 5 protein templates, CI validation | Draft v0.1 task templates |
| Workflow DAG validation | `workflow-templates` | Step/DAG consistency checks | Draft structural validation |
| Workflow artifact handoff | `workflow-templates` | `consumes` / `produces` checks across 5 protein templates | Draft executable-structure validation |
| Run record schema | `biopilot-prototype` | JSON Schema, sample run record, CI validation | Draft reproducibility record |
| BioPilot prototype | `biopilot-prototype` | MVP runbook, API draft, sample-data policy, sample-data metadata template, protocol compliance plan | Prototype plan, not full implementation |
| Landscape map | `awesome-ai4s-workflows` | 79+ related projects | Correction-friendly map |
| Position paper | `whitepaper` | position note and draft text | Framing draft |

## What has CI today

| Repository | CI check | Validates |
|---|---|---|
| `plugin-manifest` | Validate plugin manifests | Schema, command placeholders, command-template guardrails, rendering fixtures |
| `workflow-templates` | Validate workflow templates | Schema, DAG consistency, plugin list structure, artifact handoff |
| `biopilot-prototype` | Validate run records | Run-record schema against sample JSON |

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
5. Draft v0.2 command-template and run-record RFC.

## Planning references

- v0.2 RFC outline: `reference/v0.2-rfc-outline.md`
- R3 evidence template: https://github.com/OpenSciFlow/plugin-manifest/blob/main/docs/r3-evidence-template.md
- Artifact handoff validation: https://github.com/OpenSciFlow/workflow-templates/blob/main/docs/artifact-handoff-validation.md
- BioPilot compliance plan: https://github.com/OpenSciFlow/biopilot-prototype/blob/main/docs/protocol-compliance-plan.md
