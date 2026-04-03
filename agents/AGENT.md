# Main Agent

## English

`agents/AGENT.md` is the primary agent process for this repository.

### Responsibilities

- define default behavior that should always be active
- establish baseline collaboration style and operating boundaries
- stay lean and delegate specialized behavior to subagents

### Loading Model

- load this file by default
- load files from `agents/subagents/` only when the task requires that role

## 中文

`agents/AGENT.md` 是这个仓库的主 agent 进程定义。

### 职责

- 定义默认始终生效的行为
- 建立基础协作风格与运行边界
- 保持精简，把专门能力下放给子 agent

### 加载模型

- 默认加载本文件
- 只有在任务需要对应角色时，才加载 `agents/subagents/` 中的文件
