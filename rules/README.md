# Rules

## English

Store cross-project rules and guardrails here.

### What Belongs Here

- security requirements
- approval and escalation policies
- testing minimums
- review checklists

### Conventions

- Keep one topic per file.
- Write enforceable statements, not loose advice.
- Move reusable policy here when it no longer belongs to a single agent or plugin.

### Codex Loading Spec

- Codex does not automatically load arbitrary Markdown files from `rules/` as runtime instructions.
- Always-on project guidance should be exposed to Codex through `AGENTS.md` or `AGENTS.override.md`.
- Command approval rules are a different mechanism: Codex loads `.rules` files from `codex/rules/` team-config locations such as `~/.codex/rules/default.rules`, then applies them at startup.
- Task-specific reusable logic belongs in skills, not in command approval rules.

### Import This Repo's Rules Into a Codex Workspace

1. Pick the rule source from this repository, usually `rules/RULES.md` plus any topic file under `rules/`.
2. Promote the active policy into the target workspace's `AGENTS.md`; for subtree-only policy, place a nested `AGENTS.md` closer to that folder.
3. Translate shell approval or sandbox exceptions into `.rules` files under `~/.codex/rules/`.
4. Restart Codex after changing `.rules`; start a new Codex session after changing `AGENTS.md`.

### Example

```bash
# Use this repo's global rules as the target workspace instructions
ln -s /path/to/Context/rules/RULES.md /path/to/target-workspace/AGENTS.md

# Add command approval rules for the current user
mkdir -p ~/.codex/rules
cp /path/to/custom.rules ~/.codex/rules/default.rules
```

### Mapping Guide

- behavioral and review policy -> `AGENTS.md`
- folder-specific overrides -> nested `AGENTS.md`
- command allow/prompt/forbid policy -> `~/.codex/rules/*.rules`
- reusable task workflow -> `.agents/skills/`

## 中文

这个目录用于存放跨项目规则和护栏。

### 包含内容

- 安全要求
- 审批与升级策略
- 测试最低标准
- 审查清单

### 约定

- 每个文件只覆盖一个主题。
- 写可执行的规则，不写泛泛建议。
- 当某条策略不再只属于单个 agent 或插件时，就应移到这里。

### Codex 加载规范

- Codex 不会把 `rules/` 目录下的任意 Markdown 文件自动当作运行时指令加载。
- 需要始终生效的项目规则，应通过 `AGENTS.md` 或 `AGENTS.override.md` 暴露给 Codex。
- 命令审批规则是另一套机制：Codex 会在启动时加载 `codex/rules/` team-config 位置下的 `.rules` 文件，例如 `~/.codex/rules/default.rules`。
- 任务型、可复用的流程应放进 skills，而不是写进命令审批规则。

### 将本仓库的 Rules 导入 Codex 工作区

1. 先从本仓库选择规则来源，通常是 `rules/RULES.md` 加上 `rules/` 下的专题文件。
2. 将需要常驻生效的策略提升到目标工作区的 `AGENTS.md`；如果只想作用于子目录，就在更靠近该目录的位置放嵌套的 `AGENTS.md`。
3. 将命令放行、提示或禁止类策略，翻译为 `~/.codex/rules/` 下的 `.rules` 文件。
4. 修改 `.rules` 后重启 Codex；修改 `AGENTS.md` 后启动新的 Codex 会话。

### 示例

```bash
# 把本仓库的全局规则作为目标工作区说明
ln -s /path/to/Context/rules/RULES.md /path/to/target-workspace/AGENTS.md

# 为当前用户添加命令审批规则
mkdir -p ~/.codex/rules
cp /path/to/custom.rules ~/.codex/rules/default.rules
```

### 映射原则

- 行为规范和评审策略 -> `AGENTS.md`
- 目录级覆盖规则 -> 嵌套的 `AGENTS.md`
- 命令 allow/prompt/forbidden 策略 -> `~/.codex/rules/*.rules`
- 可复用任务流程 -> `.agents/skills/`
