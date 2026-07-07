# Workflow template

A workflow template describes a scientific task as ordered steps or a DAG. It references plugins, declares fallback tools, expected runtime, hardware, reproducibility metadata, and report templates.

## What It Solves

Plugin manifests describe how one tool or model can run.

Workflow templates describe how tools fit into a task.

For example, an MD stability workflow may include:

- input validation;
- trajectory loading;
- RMSD calculation;
- RMSF calculation;
- radius of gyration calculation;
- quality warnings;
- report generation;
- run-record writing.

## Required Shape

A v0.1 workflow template should include:

- task description;
- required inputs;
- expected outputs;
- steps;
- DAG dependencies;
- required and optional plugins;
- fallbacks;
- estimated runtime;
- hardware requirements;
- reproducibility requirements;
- report template;
- example dataset policy;
- limitations.

## Artifact Handoff

Each step should declare:

```text
consumes: [...]
produces: [...]
```

This prevents vague workflows where outputs appear without a producing step.

## What It Should Avoid

Avoid templates such as:

```text
discover a new drug
solve this disease
find a material with ideal properties
```

Those are research programs, not v0.1 workflow templates.

Start with narrow, repeatable tasks.

## Related Repositories

- Workflow templates: https://github.com/OpenSciFlow/workflow-templates
- Workflow review checklist: https://github.com/OpenSciFlow/workflow-templates/blob/main/docs/workflow-review-checklist.md
- Artifact handoff validation: https://github.com/OpenSciFlow/workflow-templates/blob/main/docs/artifact-handoff-validation.md
