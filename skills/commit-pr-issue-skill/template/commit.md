## Format
<type>[optional scope]: <description>

<body when needed>

<footer when needed>


## Reference
type: feat|fix|docs|style|refactor|perf|test|build|ci|chore|revert
scope: optional, use when the change is limited to a clear area
description: A short summary of the change
body: conditionally required when the description alone cannot explain the reason, context, impact, or risk of the change
footer: conditionally required for breaking changes, issue references, or migration notes

## Example

fix(auth): 修复登录状态刷新失败

刷新 token 时未同步更新本地会话，导致页面刷新后仍被识别为未登录。
现在在刷新成功后统一写入会话状态，避免认证状态和接口状态不一致。
