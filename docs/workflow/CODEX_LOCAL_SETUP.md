# Codex Desktop 本地设置

1. 安装 Git，用 Git Credential Manager 的浏览器登录或已配置的 SSH key 认证。使用 HTTPS 时，在首次需要凭据的操作中选择有目标仓库权限的账号。私钥和令牌保存在本机凭据存储中。
2. 在父目录运行以下 PowerShell 命令（派生项目替换仓库 URL 和目录名）。若已有检出，直接进入该目录并从 status 开始。

```powershell
git clone https://github.com/Bob-Wrb/Rongbo-research-workflow-template.git
cd Rongbo-research-workflow-template
git status -sb
git remote -v
git log -1 --oneline
```

3. 在 Codex Desktop 添加或打开此文件夹，选择本地工作，对照 TASK.md 确认当前分支。提交前用 `git var GIT_AUTHOR_IDENT` 检查作者配置；需要时用仓库级 `git config user.name` 和 `git config user.email` 设置自己的值。
4. 本模板为 Markdown，无运行依赖。派生 Python 项目在项目根执行下例；后两行假定项目已提供锁定版本的 requirements.txt 和对应处理脚本。根据任务填写真实脚本参数。

```powershell
py -m venv .venv
.\.venv\Scripts\python.exe --version
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\python.exe scripts/process.py --help
```

5. 使用该解释器按任务命令运行脚本，显式指定只读输入和新输出目录。在日志登记 Python、依赖版本和输入校验和；用合成样本复跑，再对照任务标准检查输出。
