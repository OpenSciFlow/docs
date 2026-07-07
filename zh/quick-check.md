# 中文快速检查清单

这个清单用于判断一个工具、模型或 workflow 是否适合加入 OpenSciFlow 草案。

## Manifest 检查

- 工具/模型名称是否明确？
- 输入文件、参数和格式是否明确？
- 输出文件、报告和日志是否明确？
- 环境依赖是否明确？
- 是否需要 GPU、HPC、Slurm 或容器？
- 模型权重来源、版本、license 和 checksum 是否明确？
- citation 是否明确？
- limitations 是否明确？

## Workflow 检查

- 任务边界是否足够窄？
- 是否能说清楚成功和失败？
- 每一步是否声明 `consumes` 和 `produces`？
- DAG 是否无环？
- fallback 是否会改变输出解释？
- report 是否会重复 citation 和 limitations？

## Local Agent 检查

- Agent 是否只执行 manifest 或 reviewed wrapper 中声明过的命令？
- 是否禁止 LLM 现场生成任意 shell 后直接执行？
- 是否在执行前展示输入、输出、命令、路径、license、citation 和限制？
- 是否需要用户批准？
- 是否把日志、版本、hash 和 artifacts 写入 run record？

## HPC / Slurm 检查

- `account`、`partition`、`time_limit` 是否明确？
- `cpu_cores`、`memory_gb`、`gpu_resources` 是否明确？
- module 或 container 是否明确？
- stdout / stderr 路径是否明确？
- wrapper script 是否已 review？
- wrapper 是否只填充允许的参数？

## 结果解释检查

- 输出是否只是计算结果，而不是实验验证？
- 是否避免临床、诊断、药效或生物功能断言？
- 是否说明模型适用范围？
- 是否说明输入数据和环境限制？

