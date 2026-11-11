# 从讨论生成 TASK.md

在 ChatGPT Project 中粘贴以下提示，并提供当前分支、SHA 和可共享的讨论记录。

```text
请依据本次讨论和仓库中的 templates/common/TASK.template.md 起草完整 TASK.md。
列出目标、范围、输入标识、允许修改的路径、原件保护要求、交付文件和实施步骤。
说明选择 Local 或 Cloud 的依据，指明依赖和基准 SHA。
为每项交付写出检查命令或人工步骤、预期结果、容差及证据位置。
保留未知项；若缺失信息会改变结论，标出需要负责人回答的问题。
输出可直接保存的 Markdown，移除敏感数据，区分建议与已确认决策。
```

负责人核对后，在任务分支保存 TASK.md 并提交、推送。向 Codex 提供仓库、任务分支、该提交 SHA 及“读取 AGENTS.md 和 TASK.md，执行并逐项报告”。
