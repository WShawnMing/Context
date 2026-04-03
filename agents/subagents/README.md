# Subagents

## English

This directory holds focused role prompts for specialized execution modes.

### Current Roles

- `coding.md`: implementation-focused execution
- `plan.md`: planning and decomposition
- `review.md`: code review and risk detection
- `test.md`: verification and test strategy

### Usage Rules

- Keep each file scoped to one role.
- Subagents are not always-on context; load them selectively by task.
- Write stable role policy, not task-specific instructions.

## 中文

这个目录用于存放面向专门执行模式的角色提示词。

### 当前角色

- `coding.md`：面向实现执行
- `plan.md`：面向规划与拆解
- `review.md`：面向代码审查与风险识别
- `test.md`：面向验证与测试策略

### 使用规则

- 每个文件只负责一个角色。
- 子 agent 不是常驻上下文，应按任务选择性加载。
- 写稳定的角色策略，不写一次性的任务说明。
