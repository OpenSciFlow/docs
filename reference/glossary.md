# Glossary

- Agent skill: instructions and schemas that teach an AI agent how to use OpenSciFlow protocol artifacts.
- Artifact: output file or directory registered by a run.
- BioPilot: the first reference prototype under OpenSciFlow, focused on local protein-computing workflows.
- Command template: reviewed command string declared in a manifest or workflow template.
- Execution request: structured record of the exact command or reviewed wrapper submission an agent proposes to run.
- Local Agent: local executor for approved workflow commands.
- Manifest-first: design principle that tools and models should declare inputs, outputs, environment, weights, citation, license, and limitations before execution.
- Model weights: files or checkpoints required by an AI model.
- OpenSciFlow Skill: agent-facing adapter layer for manifests, workflow templates, execution requests, refusal rules, and run records.
- Plugin manifest: metadata file for one tool/model.
- Readiness level: R0-R6 label describing how much evidence exists for inspection, installation, execution, citation, and reproducibility.
- Reviewed wrapper: wrapper script, such as a Slurm job script, that is declared and reviewed before an agent may render or submit it.
- Run manifest: reproducibility record for one BioPilot execution.
- Run record: audit record for a tool or workflow run, including commands, versions, inputs, outputs, logs, hashes, citation, license, limitations, and warnings.
- Slurm: HPC scheduler commonly used for cluster jobs.
- Workflow template: reusable task plan with inputs, outputs, steps, DAG, plugins, fallbacks, reproducibility requirements, and limitations.
