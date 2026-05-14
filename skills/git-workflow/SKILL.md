---
name: git-workflow
description: commit、PR、issue、tag、branch 工作流规范技能，生成相关内容时使用
---

# Git Workflow

生成 commit、PR、issue、tag 内容和 branch 命名时使用。

- 不写提交人、协作者、工具来源或 AI 署名。
- 除固定关键词外，使用中文。

## Branch

- 默认分支为 `main`，不直接在 `main` 上提交。
- 提交前从 `main` 创建工作分支，并通过 PR 合并回 `main`。
- 分支命名使用 `<type>/<short-kebab-summary>`。
- 如果分支包含多类改动，使用主要改动类型；难以归类时使用 `chore`。
- 示例：`docs/update-pr-template`、`fix/remove-codex-prefix`、`feat/add-tag-template`。

示例：

- [commit](./template/commit.md)
- [pull request](./template/pull_request.md)
- [issue](./template/issue.md)
- [tag](./template/tag.md)
