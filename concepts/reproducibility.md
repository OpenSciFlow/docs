# Reproducibility

Every OpenSciFlow run should record task text, workflow version, plugin versions, input hashes, commands, tool versions, environment, output hashes, citations, and limitations.

## Why This Matters

AI for Science workflows often fail reproducibility for practical reasons:

- exact model weights are unclear;
- package versions are not recorded;
- command-line parameters are missing;
- input files change;
- output files are copied without hashes;
- reports omit citations or limitations;
- cluster jobs hide stdout and stderr paths.

OpenSciFlow treats run records as first-class protocol artifacts.

## Minimum Record

A useful run record should include:

- run id;
- workflow id;
- plugin manifest id;
- start and finish timestamps;
- status;
- commands;
- inputs and hashes;
- outputs and hashes where available;
- versions;
- environment;
- model weights;
- hardware;
- logs;
- artifacts;
- citations;
- licenses;
- limitations;
- warnings.

## Planned vs Completed Records

A planned record is allowed.

It must not be confused with execution evidence.

For example, a BioPilot planning response may say:

```text
status: blocked
reason: MDAnalysis is R2 but request requires R3
```

That is useful evidence because it prevents premature execution claims.

## Related Repositories

- BioPilot run-record schema: https://github.com/OpenSciFlow/biopilot-prototype/blob/main/schema/opensciflow-run-record.schema.json
- Skill run-record alignment: https://github.com/OpenSciFlow/opensciflow-skill/blob/main/docs/run-record-alignment.md
