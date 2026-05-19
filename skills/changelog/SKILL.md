---
name: changelog
description: 用于记录项目开发和发布过程中的有意义变更，并维护 changelog、版本记录和发布说明。
---

# Changelog

## Rule

- 除固定关键词外，使用中文。
- 默认维护仓库根目录 `CHANGELOG.md`。
- 有意义的用户或工程变更，写入对应 `CHANGELOG.md` 的 `[Unreleased]` 区块；没有该区块时先创建。
- 发布 tag 时，将当前 `[Unreleased]` 标题改为 `[<version>] - <YYYY-MM-DD>`。
- 维护 `[Unreleased]` 时，遵循下面的合并规则。

## Unreleased 合并规则

- **重点：`[Unreleased]` 中尚未发布的条目发生后续调整时，只修改原条目，让它描述最终状态，不要新增一条记录来描述这次调整。**
- **本周期** 指当前 `CHANGELOG.md` 的 `[Unreleased]` 区块，也就是从上一次发布到下一次发布之间尚未发布的所有变更；不是一次对话、一次提交、一天或当前任务。
- `[Unreleased]` 不是操作日志，而是下一次发布后的最终变更说明；分类按最终发布内容选择，不按开发过程选择。
- 写入 changelog 前，先检查 `[Unreleased]` 中是否已有条目描述同一功能、同一行为或同一工程变更。
- 如果已有相关条目，本次改动只是补充、调整、修正或完善它，则只编辑原条目；只有没有归属关系且需要在下一次发布中告知的独立变更，才新增条目。
- 例如：本周期在 `Added` 中记录了一个新功能，随后修复这个新功能本身的问题时，应直接更新该 `Added` 条目，使其描述修复后的最终功能，不要再新增 `Fixed`。
- 同一原则适用于所有 `[Unreleased]` 分类：如果后续改动是在完善、调整或修正本周期已记录的 `Changed`、`Deprecated`、`Removed`、`Security` 等条目，也应更新原条目，而不是新增另一条过程记录。

## Template

```markdown
# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added

<!-- 新添加的功能。 -->

-

### Changed

<!-- 对现有功能的变更。 -->

-

### Deprecated

<!-- 已经不建议使用、未来会移除的功能。 -->

-

### Removed

<!-- 已经移除的功能。 -->

-

### Fixed

<!-- 对 bug 的修复。 -->

-

### Security

<!-- 对安全性的改进。 -->

-

## [<version>] - <YYYY-MM-DD>

...
```
