# Agents

## English

This directory stores the main agent definition and the subagent registry.

### What Belongs Here

- `AGENT.md`: the primary agent process and default always-on behavior
- shared agent policies visible before any subagent is loaded
- specialized prompts under `subagents/`

### Conventions

- Keep `AGENT.md` broad and stable.
- Do not embed all specialized behavior into the main file.
- Add specialized behavior as `agents/subagents/<role>.md` and load it only when needed.

## 中文

这个目录用于存放主 agent 定义以及子 agent 注册结构。

### 包含内容

- `AGENT.md`：主 agent 进程和默认常驻行为
- 在任何子 agent 加载前都应可见的共享策略
- 放在 `subagents/` 下的专用角色提示词

### 约定

- `AGENT.md` 保持宽口径且稳定。
- 不要把所有专用行为都塞进主文件。
- 专门能力放到 `agents/subagents/<role>.md`，仅在需要时加载。
