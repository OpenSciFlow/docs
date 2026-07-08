# Check Before Run, Record After Run

OpenSciFlow follows a simple rule:

```text
check before run
record after run
```

This rule is stricter than simply storing a manifest.

## Check Before Run

Before execution, an agent or runner should check:

- manifest schema;
- required inputs;
- environment requirements;
- hardware requirements;
- model-weight source, license, and checksum status;
- reviewed command template or reviewed wrapper metadata;
- license and citation metadata;
- known failure cases;
- verified environment matrix;
- output directory and write permissions;
- user approval requirements.

If required metadata is missing, the runner should fail closed.

## Record After Run

After a dry run, smoke test, example run, or full run, the runner should write a run record.

The run record should include:

- capsule id;
- manifest id;
- workflow id, if applicable;
- command source;
- rendered command;
- input paths and hashes;
- output paths and hashes;
- tool versions;
- environment information;
- hardware information;
- model weights;
- logs;
- return code;
- timestamps;
- citations;
- licenses;
- limitations;
- warnings;
- known failures encountered.

## What This Does Not Promise

This does not eliminate scientific computing failures.

It makes failures and successful runs explicit, checkable, diagnosable, and recordable.
