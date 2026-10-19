# GitHub issue 记录与跟踪

- 当用户提出项目需求、报告 Bug，或发起关于本项目的咨询讨论时，主动在本项目对应的 GitHub 仓库创建 issue，用于记录和跟踪。
- 用户已授权上述 issue 创建行为，无需每次再次确认。
- 创建前先检查是否已有对应 issue；若已有，优先补充已有 issue，避免重复创建。
- 根据消息内容整理清晰的标题和正文，记录背景、需求或问题、已知信息和待办。Bug 应在信息可用时包含复现步骤、预期行为和实际行为；咨询讨论应记录讨论主题、待确认事项及已达成的结论。不要编造缺失信息。
- 创建或更新完成后，将 issue 链接反馈给用户；后续相关工作继续在对应 issue 中记录进展与结论。
- 若无法确定对应仓库，或 GitHub 访问权限、工具不可用，明确说明尚未创建或更新 issue 及原因，不要声称已完成记录。

## 标题、类型与标签

- 一次提问只建一条 issue；同一话题的追问写成评论，不另开 issue。被派去执行具体任务的子代理不建 issue，由直接面对用户的会话负责记录。
- 标题格式 `<type>(<scope>): <description>`，对齐 Conventional Commits：scope 可选，用英文小写（如 `admin`、`post`、`identity`），没有明确范围就写成 `<type>: <description>`；description 简短说明要解决的问题，结尾不加句号。例：`fix(admin): 表单点确定无反应`。
- 选一个主要类型决定标题 type，其余类型只作为标签加上。标签不存在就先创建，不能跳过：

| 类型 | 标签 | 标题 type | 用途 |
| --- | --- | --- | --- |
| Bug | bug | fix | 已有功能出现错误 |
| Feature | feature | feat | 原来没有的新功能 |
| Improvement | enhancement | feat | 改进已有功能 |
| Documentation | documentation | docs | 文档新增或修改 |
| UI/UX | ui | fix 或 feat | 界面、交互问题：已经坏了用 fix，新增交互用 feat |
| Refactor | refactor | refactor | 重构，不改变功能 |
| Performance | performance | perf | 性能优化 |
| Test | test | test | 测试相关 |
| Security | security | fix | 漏洞或泄露（同时是功能错误时再加 `bug`） |
| Chore | chore | chore | 工程、依赖、配置、发布等维护 |
| Question | question | question | 使用咨询、技术问题 |
| Discussion | discussion | discussion | 需要讨论后决定 |

- UI/UX 只是次要类型时，标题 type 跟随主要类型，`ui` 作为标签加上。

## 正文

- 依次写三段：`## 来源`（本次会话所在的工具，如 Cursor、Claude Code）、`## 提问`（用户原文）、`## 回复要点`（结论，不贴推理过程）。仓库 issue 模板要求的其它内容接在后面补充。
- 只把具体的密钥值替换为 `[REDACTED]`，标题、正文和评论里都不出现这些值；“token”“密码”这类词本身不需要打码。
- 实现某个 issue 的 PR 在描述里写 `Closes #<编号>`。
