# FAQ

## Is OpenSciFlow a replacement for workflow engines?

No. It should interoperate with existing workflow engines.

## Is BioPilot the same as OpenSciFlow?

No. BioPilot is the first reference prototype. OpenSciFlow is the broader initiative.

## Is OpenSciFlow a mature standard?

No. It is an early public draft. The current goal is correction-first review.

## Can an agent execute arbitrary shell commands?

No. The local-agent principle is to execute only reviewed command templates or reviewed wrapper submissions declared in protocol artifacts.

## Does OpenSciFlow certify scientific correctness?

No. It records execution metadata, citations, licenses, artifacts, and limitations. It does not certify that a model output is experimentally true.

## Why use normalized scheduler fields?

OpenSciFlow-facing files use fields such as `time_limit`, `cpu_cores`, `memory_gb`, and `gpu_resources`. A reviewed wrapper maps them to Slurm-specific options such as `--time`, `--cpus-per-task`, `--mem`, and `--gres`.

## Why are some fields required even when they are not applicable?

Because missing metadata is ambiguous. A manifest should say `not-applicable`, `user-provided`, `unknown`, or `to-be-filled` instead of silently omitting execution-relevant information.
