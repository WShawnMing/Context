# Vibe Coding Context Repo

This repository is used to version and manage all supplemental context required for vibe coding workflows.

## Scope

- `Agent.md`: primary agent-facing context and operating preferences
- `RULES.md`: global rules and guardrails
- `skills/`: reusable skill definitions or prompt modules
- `plugins/`: plugin-level configuration and integration notes
- `rules/`: split rule sets by topic or tool
- `contexts/`: project-, client-, or task-specific context packs

## Management Model

Everything here is meant to be addable, reviewable, and removable through normal Git operations.

- Add new context as a small, focused file or folder in the most specific directory.
- Update related indexes or READMEs when structure changes.
- Delete stale context by removing the corresponding file or directory in the same commit.

## Suggested Naming

- Use lowercase kebab-case for folders, for example `skills/pr-review/`
- Use descriptive Markdown filenames, for example `contexts/acme-onboarding.md`
- Keep one concern per file where possible
