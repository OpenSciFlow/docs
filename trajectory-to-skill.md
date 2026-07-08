# Trajectory to Skill

OpenSciFlow should not be built by writing manifests from scratch in isolation.

The stronger path is:

```text
successful run trajectory
-> extract reusable steps
-> remove machine-specific assumptions
-> generate manifest + command templates + environment spec
-> validate schemas
-> run smoke tests
-> execute example run
-> write run record
-> publish verified execution capsule
-> optionally distill into OpenSciFlow Skill
```

## What Counts as a Run Trajectory?

A run trajectory is the practical record of how a tool was made to run:

- commands attempted;
- environment setup;
- package versions;
- model-weight paths and checksums;
- input files;
- output files;
- errors and fixes;
- final command;
- logs;
- return code;
- runtime;
- machine or cluster context.

## What Should Be Extracted?

From a successful trajectory, extract:

- the minimal task boundary;
- stable inputs and outputs;
- reviewed command template;
- environment requirements;
- smoke test;
- expected artifacts;
- citations and licenses;
- limitations;
- known failures.

## What Should Be Removed?

Remove or mark machine-specific assumptions:

- private usernames;
- private filesystem paths;
- site-specific Slurm accounts;
- non-portable module names unless declared as site-specific;
- local cache paths;
- untracked model-weight locations;
- unstated permissions;
- undocumented driver/CUDA assumptions.

## Skill Distillation

Only after the capsule has enough evidence should it be distilled into an OpenSciFlow Skill.

The skill should teach an agent how to inspect the capsule, check environment readiness, select reviewed commands, run smoke tests, request approval, write run records, and report known failures.

It should not teach the agent to improvise shell commands or claim that a new environment will work before evidence exists.
