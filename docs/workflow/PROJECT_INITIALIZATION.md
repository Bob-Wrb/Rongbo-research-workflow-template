# 用模板创建项目

1. 依照 [GitHub 设置](GITHUB_SETUP.md)启用模板属性。选择 Use this template → Create a new repository，填写 owner、项目名和可见性，创建后核对 README 与默认分支。
2. 按 [Local 设置](CODEX_LOCAL_SETUP.md)克隆新仓库，核对 origin 指向新项目，建立 `docs/project-context` 分支。
3. 选择 templates/ 下的研究、论文、实验或教学 README 作为写作提纲。软件开发直接使用通用任务单。对照 templates/common/ 填写根目录 PROJECT_CONTEXT.md、DECISIONS.md、WORK_LOG.md，替换模板项目的目标、所有者和日志。
4. 从 templates/common/TASK.template.md 复制生成根目录 TASK.md。写入首项任务，例如“用合成输入验证脚本”，给出命令、预期和证据路径。
5. 在 ChatGPT 新建同名 Project，在项目说明写入仓库标识、默认分支、上下文文件及复核方式。连接 GitHub 并验证能读取 README 和当前上下文；也可提供带 SHA 的脱敏快照。
6. 提交并通过 PR 审查建项改动。按 [Cloud 设置](CODEX_CLOUD_SETUP.md)创建环境，分别在 Local 与 Cloud 读取同一提交的 README 标题并比较 SHA。将结果及任何访问限制记入工作日志。
7. 从下一项任务开始，按[系统架构](ARCHITECTURE.md)执行完整交接。
