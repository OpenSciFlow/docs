# What Is OpenSciFlow?

OpenSciFlow is an early open initiative for building verified execution capsules for AI for Science tools.

It does not promise that scientific tools will run everywhere. Instead, it makes tool requirements, environment assumptions, verification status, run records, and known failures explicit and machine-readable.

## Core Idea

OpenSciFlow starts from a stricter execution loop:

```text
verified execution capsule
-> check requirements and known failures
-> run smoke test when available
-> render reviewed command template
-> execute after approval
-> write run record
```

## Main Artifacts

- Verified execution capsule: execution-facing package with manifest, environment spec, command templates, smoke tests, run records, verified environment matrix, and known failures.
- `opensciflow.yaml`: manifest for one scientific tool or model.
- Workflow template: reusable task plan with inputs, outputs, steps, DAG, plugins, fallbacks, and limitations.
- Execution request: exact reviewed command or wrapper submission proposed by an agent.
- Run record: audit record containing commands, versions, inputs, outputs, logs, hashes, citations, licenses, limitations, and warnings.
- OpenSciFlow Skill: agent-facing adapter that teaches AI agents how to inspect capsules and use the protocol safely.
- BioPilot: first reference prototype for local protein-computing workflows.

## Design Principles

- Capsule-first.
- Check-before-run.
- Record-after-run.
- Local-first.
- Correction-first.
- No arbitrary LLM-generated shell execution.

## Current Stage

OpenSciFlow is an early public draft.

The current goal is to make the protocol reviewable and correctable before asking anyone to adopt it.
