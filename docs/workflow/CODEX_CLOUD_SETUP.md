# Codex Cloud 设置

1. 在 Codex 的云端环境设置中连接 GitHub，授权选定仓库。确认列表出现正确的 owner/name，选择仓库创建环境。组织账号可能需要管理员批准应用。
2. 本模板只需 Git 和文本工具。派生项目按其依赖清单配置运行时与 setup 命令，例如已有锁定版本的 requirements.txt 时运行 `python -m pip install -r requirements.txt`。在环境日志核对安装结果；按实际需要设置网络范围和 secrets，避免记录值。
3. 将任务和脱敏输入提交并推送到任务分支，在云端选择该分支、环境并发起任务。每项云任务有独立工作区；通过 Git 或获准的产物存储交接文件。
4. 首次用只读任务验收：“运行下列命令，报告起始 SHA、环境和 README 标题”。将 SHA 与预期基准核对。

```sh
git rev-parse HEAD
git status --short
head -n 1 README.md
```

5. 后续写任务附 TASK.md 路径与验收表；检查差异、测试日志，并用可用的 PR 入口发布到 GitHub。遇到权限或网络限制，报告实际状态与未运行项。具体入口随账号和产品版本而异。[OpenAI 云环境文档](https://developers.openai.com/codex/cloud/environments)
