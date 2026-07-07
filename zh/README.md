# OpenSciFlow 中文文档入口

OpenSciFlow 是一个面向 AI for Science workflow 的早期开源倡议。

它当前关注的不是“自动科学发现”，而是更基础的一层协议：

```text
工具/模型 manifest
-> workflow template
-> 本地或 HPC 执行请求
-> run record
-> 可审计、可引用、可复现的报告
```

## 先读什么

建议按这个顺序阅读：

1. `../README.md`
   - 总入口。
2. `../reference/protocol-status.md`
   - 当前已经做到什么，哪些还没有做到。
3. `../concepts/plugin.md`
   - 什么是 `opensciflow.yaml`。
4. `../concepts/workflow-template.md`
   - workflow template 解决什么问题。
5. `../concepts/local-agent.md`
   - 本地 Agent 应该如何执行，哪些事情不能做。
6. `../concepts/reproducibility.md`
   - 为什么每次运行都要留下 run record。
7. `../reference/v0.2-reviewed-wrapper-rfc.md`
   - Slurm / wrapper script 的当前草案。

## 中文定位

OpenSciFlow 的目标是让科研模型和工具能被本地 Agent 安全调用、完整记录、正确引用，并在本地服务器或 HPC 上可复现运行。

它当前最重要的三个原则是：

- **manifest-first**：先把工具/模型的输入、输出、环境、权重、许可证、引用和硬件需求说清楚。
- **local-first**：优先在用户本地工作站、实验室服务器或 HPC 上运行，数据不默认上传到外部平台。
- **reproducibility-first**：每次运行都记录命令、版本、参数、日志、产物、hash、引用和限制。

## 现在有什么

截至当前公开草案，OpenSciFlow 已经包含：

- `plugin-manifest`：工具/模型 manifest 草案。
- `workflow-templates`：蛋白计算和材料/原子模拟 workflow template 草案。
- `opensciflow-skill`：面向 AI Agent 的协议适配层。
- `biopilot-prototype`：第一个本地蛋白计算 reference prototype。
- `awesome-ai4s-workflows`：AI for Science 相关项目地图。
- `docs`：概念、路线图、RFC、贡献入口。
- `community`：外联、贡献队列和社区流程。

## 当前不要误解

OpenSciFlow 现在仍然是 early public draft。

它不是：

- 成熟标准；
- 通用 AI Scientist；
- workflow engine 的替代品；
- 临床、诊断或药物研发决策系统；
- 对 listed projects 的合作声明。

## 怎么参与

当前最需要的是纠错，不是背书。

适合提交 issue 的问题包括：

- manifest 字段是否缺失；
- license / citation / model weight metadata 是否表达正确；
- Slurm / HPC 字段是否足够；
- local-agent refusal rule 是否安全；
- workflow output 是否容易被误解；
- 哪些项目描述、引用或链接不准确。

贡献入口：

- `../reference/contribution-routes.md`
- `../../community/contribution-queue.md`

