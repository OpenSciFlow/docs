# Plugin manifest

A plugin manifest describes one scientific tool or model: what it does, what inputs/outputs it expects, how to run it, what environment it needs, how to validate it, how to cite it, and what limitations apply.

The default filename is:

```text
opensciflow.yaml
```

## What It Solves

Scientific tools often require users to read long READMEs, issue threads, paper supplements, install notes, model cards, and cluster-specific scripts before a local agent can safely call them.

A plugin manifest compresses the minimum executable metadata into one reviewable file.

## What It Should Contain

A useful v0.1 manifest should describe:

- tool or model name;
- supported task types;
- required and optional inputs;
- expected outputs;
- environment requirements;
- hardware requirements;
- model weights, if any;
- local command templates;
- optional Slurm / HPC wrapper metadata;
- dry-run and smoke-test commands;
- citation;
- software, model-weight, and data license metadata;
- safety notes;
- scientific limitations.

## What It Is Not

A plugin manifest is not:

- an upstream project endorsement;
- a certification of scientific correctness;
- permission to ignore upstream licenses;
- a replacement for upstream documentation;
- a reason for an agent to execute arbitrary shell.

## Readiness

Manifests should move slowly through readiness levels:

```text
R1 schema-ready
R2 metadata-reviewed
R3 dry-run-ready
R4 smoke-test-ready
R5 run-record-ready
R6 workflow-ready
```

A famous or widely used tool does not automatically get a high readiness level. Evidence is required.

## Related Repositories

- Plugin manifest draft: https://github.com/OpenSciFlow/plugin-manifest
- Readiness levels: https://github.com/OpenSciFlow/plugin-manifest/blob/main/docs/readiness-levels.md
- Validation levels: https://github.com/OpenSciFlow/plugin-manifest/blob/main/docs/validation-levels.md
- Manifest review checklist: https://github.com/OpenSciFlow/plugin-manifest/blob/main/docs/manifest-review-checklist.md
