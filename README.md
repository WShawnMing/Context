# Vibe Coding Context Repo

## English

This repository stores reusable context for vibe coding workflows and keeps it versioned, reviewable, and removable with normal Git operations.

### Layout

- `agents/`: agent system definitions; `agents/AGENT.md` is the primary entrypoint and `agents/subagents/` contains selectively loaded subagents
- `skills/`: reusable skills; third-party skill repositories should be linked as submodules
- `plugins/`: plugin manifests, integration notes, and connector-specific configuration
- `rules/`: cross-project rules, policies, and guardrails
- root documents: repository-level guides and operating notes

### Operating Rules

- Put each concern in the narrowest directory that owns it.
- Prefer small Markdown files over one oversized document.
- Remove stale context in the same commit that replaces it.
- Update the nearest `README.md` when structure changes.

### Naming

- Use lowercase kebab-case for directories.
- Use descriptive Markdown filenames.
- Use submodules instead of copying third-party repositories.

### Submodules

Clone with `git clone --recurse-submodules <repo-url>`.

If already cloned, run `git submodule update --init --recursive`.

## 中文

这个仓库用于管理 vibe coding 所需的可复用上下文，并通过 Git 进行版本化、评审和删除。

### 目录结构

- `agents/`：Agent 体系定义；`agents/AGENT.md` 是主入口，`agents/subagents/` 存放按需加载的子 agent
- `skills/`：可复用 skill；第三方 skill 仓库优先以子模块方式接入
- `plugins/`：插件清单、集成说明和连接器配置
- `rules/`：跨项目规则、策略和护栏
- 根目录文档：仓库级说明和运行约定

### 管理规则

- 每类内容放在最小且最明确的归属目录中。
- 优先使用小而清晰的 Markdown 文件，不要堆成一个超大文档。
- 替换旧内容时，在同一个提交中移除过期内容。
- 目录结构变化时，同时更新最近的 `README.md`。

### 命名约定

- 目录统一使用小写 kebab-case。
- Markdown 文件名应具备明确语义。
- 第三方仓库使用子模块，不直接复制代码。

### 子模块

首次克隆使用 `git clone --recurse-submodules <repo-url>`。

如果仓库已经存在，本地执行 `git submodule update --init --recursive`。
