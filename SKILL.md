---
name: wukong-code-projects
description: 悟空的项目协作规则：规范驱动开发（SDD）、测试先行（TDD）、根因调试、完成前验证、GitHub issue 记录与 Project 看板同步。在任何代码项目里写需求/spec/计划、写或改功能代码、修 Bug、重构、声称完成、提交或开 PR、建 issue 时使用。
---

# wukong-code-projects

通用项目协作规则，适用于任何代码仓库。以下规则每次都要遵守；细则在 `references/` 下，做对应的事之前先读相应文件，不需要时不必读。

若目标项目自己的 `AGENTS.md` / `CLAUDE.md` 与本 skill 冲突，以项目文件为准（尤其是测试命令、仓库地址、Project 看板链接）。

## 始终遵守

- 每次执行结束后，在最终回复中附带“推荐下一步做什么”，根据当前进展给出具体、可执行的下一步建议。
- 用户提出需求、报告 Bug 或咨询讨论时，主动在本项目的 GitHub 仓库建 issue 或补充已有 issue（用户已授权，无需再确认），并把链接反馈给用户。
- 先有经用户批准的 spec 再写代码（SDD）；先写会失败的测试再实现（TDD）；没找到根因不修 Bug；没实际运行检查不声称完成。
- 用到的工具或权限不可用时，如实说明没做成什么，不声称已完成。
- 写代码时说清假设，只写解决问题所需的最少代码，每一行改动都能追溯到需求。

## 按需读取

| 什么时候 | 读哪个文件 |
| --- | --- |
| 新功能或较大行为变更，要写产品需求文档（做什么、为什么、验收标准） | [references/prd.md](references/prd.md) |
| 新功能、行为变更或需求不清，要写 spec 或实施计划 | [references/sdd.md](references/sdd.md) |
| 用户明确要求逐题追问、深入澄清 | [references/grilling.md](references/grilling.md) |
| 写或改功能代码、修 Bug、重构 | [references/tdd.md](references/tdd.md)、[references/coding.md](references/coding.md) |
| 遇到 Bug、测试失败或意外行为 | [references/debugging.md](references/debugging.md) |
| 准备声称完成、提交或开 PR；处理评审意见 | [references/verification.md](references/verification.md) |
| 新建或更新 GitHub issue（标题、标签、正文） | [references/issues.md](references/issues.md) |
| 建 issue / PR 后同步 Project 看板，查历史设计与计划 | [references/github-projects.md](references/github-projects.md) |
