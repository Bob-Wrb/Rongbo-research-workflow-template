# GitHub 设置

1. 打开目标仓库，核对 owner/name 和默认分支。在 Settings → General 勾选 Template repository，刷新后确认显示 Use this template。此步骤需要仓库管理权限。
2. 选择可见性。公开模板只存可公开材料；私有项目将成员和应用限制到所需仓库。原始数据、凭据和保密文件均存于独立受控位置。
3. 在 GitHub 的已安装应用设置中，对 ChatGPT 和 Codex 分别核对所选仓库。用 ChatGPT 读取 README；用执行账号核对仓库写权限。切换账号后重新核对授权。
4. 在本地核对 remote 与分支。从干净的 main 开始常规任务，按任务选择 feat/、fix/、paper/、fig/ 或 docs/ 前缀。示例：

```sh
git switch main
git pull --ff-only
git switch -c docs/update-context
# 修改 PROJECT_CONTEXT.md 后
git add PROJECT_CONTEXT.md
git diff --cached
git commit -m "docs: clarify project scope"
git push -u origin docs/update-context
git rev-parse HEAD
git ls-remote origin refs/heads/docs/update-context
```

5. 两个 SHA 相同后在 GitHub 选择 Compare & pull request，base 选 main，填写验收结果和未决项。负责人审查后合并。可在 Settings → Rules 为 main 设置 PR 审查；按项目需要选择已有的状态检查。推送被拒时先 fetch 并检查分叉，禁止 force-push。
