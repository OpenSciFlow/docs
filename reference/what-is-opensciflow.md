# What Is OpenSciFlow?

OpenSciFlow is an early open initiative for AI for Science workflows.

It focuses on a protocol layer that helps scientific tools and models become easier to:

- inspect;
- run locally or on HPC;
- cite;
- validate;
- record;
- reproduce.

## Core Idea

OpenSciFlow starts from a simple stack:

```text
plugin manifests
-> workflow templates
-> reviewed execution requests
-> run records
-> reports with citations and limitations
```

## Main Artifacts

- `opensciflow.yaml`: manifest for one scientific tool or model.
- Workflow template: reusable task plan with inputs, outputs, steps, DAG, plugins, fallbacks, and limitations.
- Execution request: exact reviewed command or wrapper submission proposed by an agent.
- Run record: audit record containing commands, versions, inputs, outputs, logs, hashes, citations, licenses, limitations, and warnings.
- OpenSciFlow Skill: agent-facing adapter that teaches AI agents how to use the protocol safely.
- BioPilot: first reference prototype for local protein-computing workflows.

## Design Principles

- Manifest-first.
- Local-first.
- Reproducibility-first.
- Correction-first.
- No arbitrary LLM-generated shell execution.

## Current Stage

OpenSciFlow is an early public draft.

The current goal is to make the protocol reviewable and correctable before asking anyone to adopt it.

