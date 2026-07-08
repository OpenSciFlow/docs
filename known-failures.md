# Known Failures

Known failures are part of the OpenSciFlow evidence model.

They should not be hidden. They make execution safer by showing where a capsule is not ready.

## Examples

- CUDA version mismatch.
- GPU driver incompatibility.
- Conda solver failure.
- Missing model weights.
- Model-weight checksum mismatch.
- License or citation ambiguity.
- HPC module unavailable.
- Slurm account or partition unknown.
- Docker unavailable on the cluster.
- Apptainer image build failure.
- Permission error on shared filesystem.
- Input file format mismatch.
- Tool version changed output layout.

## Failure Record Fields

A known failure record should include:

- capsule id;
- tool or model version;
- environment;
- command or step;
- observed error;
- likely cause;
- workaround, if known;
- whether execution was attempted;
- whether outputs were produced;
- date observed;
- reporter or source.

## Agent Rule

Before proposing execution, an agent should check known failures.

If a known failure matches the current environment or input condition, the agent should warn or refuse execution and propose a safe next action.

The agent should not treat an untested environment as successful.
