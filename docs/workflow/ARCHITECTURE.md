# 架构与信息流

ChatGPT Project → TASK.md → GitHub → Codex Local / Cloud → Validation → Git Commit → ChatGPT Review

| 环节 | 责任与可检查的交接物 |
| --- | --- |
| 讨论 | 研究者在 Project 比较方案，明确证据、限制和交付物 |
| 固化任务 | 将结论写入 TASK.md，标记未决项，提交任务分支并传递 SHA |
| 分配执行 | Local 打开对应检出目录，Cloud 选择可访问的仓库和分支；执行前比对基准 |
| 验证 | 对每条验收项记录命令、实际输出、证据路径及偏差 |
| 版本化 | Codex 检查差异、提交、推送并创建 PR，报告实际状态 |
| 独立复核 | ChatGPT 对照任务、差异及证据提出意见；负责人决定是否合并 |

聊天历史保留讨论过程。跨环境工作的持久依据是仓库中的 PROJECT_CONTEXT.md、DECISIONS.md、TASK.md 与 WORK_LOG.md。聊天里改变范围时，先更新任务和验收项。ChatGPT 的 GitHub 连接在本流程中主要用于读取和分析；文件修改和 Git 操作交给 Codex 在获授权的工作区完成。复核无法访问分支时，提供脱敏差异和测试摘要。
