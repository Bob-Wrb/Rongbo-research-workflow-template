# Rongbo 统一科研工作流 v1.0

用一个 Git 仓库保存项目约定、任务、证据索引和审查记录。模板只含公开示例，可用于研究、论文、实验处理、软件开发与教学。

## 从这里开始

1. 按[新项目初始化](docs/workflow/PROJECT_INITIALIZATION.md)生成自己的仓库。
2. 填写[项目上下文](PROJECT_CONTEXT.md)，选用下方项目示例。
3. 在 ChatGPT Project 中讨论问题，按[任务交接](docs/workflow/CHATGPT_TO_CODEX.md)形成 TASK.md。
4. 按[环境选择](docs/workflow/LOCAL_VS_CLOUD.md)分配执行位置。Codex 遵循[执行规则](AGENTS.md)修改、验证并提交。
5. 复核 PR 和[执行记录](WORK_LOG.md)，按[独立复核](docs/workflow/CODEX_TO_CHATGPT.md)反馈，长期约定记入[决策记录](DECISIONS.md)。

| 指南 | 使用时机 |
| --- | --- |
| [系统架构](docs/workflow/ARCHITECTURE.md) | 了解每次交接的输入与输出 |
| [GitHub 设置](docs/workflow/GITHUB_SETUP.md) | 配置权限、模板与分支 |
| [Codex Local](docs/workflow/CODEX_LOCAL_SETUP.md) | 使用本机仪器、私有输入或桌面软件 |
| [Codex Cloud](docs/workflow/CODEX_CLOUD_SETUP.md) | 在独立环境复现公开任务 |

## 项目示例

[研究计划](templates/research-project/README.md) · [论文写作](templates/paper-project/README.md) · [实验处理](templates/experiment-project/README.md) · [课程制作](templates/teaching-project/README.md)

软件任务使用[通用任务单](templates/common/TASK.template.md)，填写受影响接口、兼容性要求、复现步骤及测试命令。许可协议待所有者决定。
