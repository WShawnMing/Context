# Skills

## English

Store reusable skills in this directory.

### Local Skills

Use a dedicated folder per skill, for example:

- `skills/pr-review/SKILL.md`
- `skills/release-checklist/SKILL.md`

### Third-Party Skills

Do not copy external skill repositories into this repo. Add them as Git submodules so upstream history, authorship, and licensing remain intact.

Current example:

- `skills/pua/` -> submodule from `https://github.com/tanweai/pua`

### Common Commands

- initialize submodules: `git submodule update --init --recursive`
- update one skill: `git submodule update --remote --merge skills/pua`

## 中文

这个目录用于存放可复用的 skill。

### 本地 Skill

每个 skill 使用独立目录，例如：

- `skills/pr-review/SKILL.md`
- `skills/release-checklist/SKILL.md`

### 第三方 Skill

不要把外部 skill 仓库直接复制进来。应使用 Git 子模块接入，以保留上游历史、作者归属和许可证边界。

当前示例：

- `skills/pua/` -> 来自 `https://github.com/tanweai/pua` 的子模块

### 常用命令

- 初始化子模块：`git submodule update --init --recursive`
- 更新单个 skill：`git submodule update --remote --merge skills/pua`
