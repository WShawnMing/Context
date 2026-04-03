# Plugins

## English

Store plugin-specific configuration and operating notes here.

### Recommended Structure

- `plugins/<plugin-name>/README.md`: usage and maintenance notes
- `plugins/<plugin-name>/plugin.json`: manifest or local metadata
- `plugins/<plugin-name>/examples/`: optional examples or templates

### Conventions

- Keep one directory per plugin.
- Separate plugin config from agent rules and generic skills.
- Document required credentials and scopes in the plugin's own `README.md`.

## 中文

这个目录用于存放插件级配置和运行说明。

### 推荐结构

- `plugins/<plugin-name>/README.md`：使用和维护说明
- `plugins/<plugin-name>/plugin.json`：清单或本地元数据
- `plugins/<plugin-name>/examples/`：可选示例或模板

### 约定

- 每个插件独立一个目录。
- 插件配置与 agent 规则、通用 skill 分开管理。
- 需要的凭据和权限范围写在插件自己的 `README.md` 中。
