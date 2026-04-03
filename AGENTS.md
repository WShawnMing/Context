# Repository Guidelines

## Project Structure & Module Organization
This workspace is currently empty and does not yet contain source code, tests, or assets. Keep the top level minimal as the project grows. Place application code in `src/`, automated tests in `tests/`, reusable static files in `assets/`, and longer-form documentation in `docs/`. Mirror the structure of `src/` inside `tests/` so ownership stays obvious; for example, `src/api/client.ts` should pair with `tests/api/client.test.ts`.

## Build, Test, and Development Commands
No build system or task runner is configured in the current repository. When adding one, expose the common workflows through stable top-level commands and update this guide in the same change. Preferred examples are `make test`, `npm test`, `pytest`, or another single entry point that a new contributor can run without guesswork. If a setup step is required, document it in `README.md` and keep local bootstrap commands deterministic.

## Coding Style & Naming Conventions
Use 2 spaces for Markdown, YAML, and JSON indentation; use the formatter or language standard for everything else. Name directories and modules with lowercase kebab-case or snake_case, depending on language norms, and reserve PascalCase for types, classes, or components. Keep filenames descriptive and feature-oriented, such as `src/auth/session_manager.py` or `src/ui/user-card.tsx`. Add a formatter and linter early, then run them before opening a review.

## Testing Guidelines
Add automated tests alongside each new feature or bug fix. Prefer fast unit tests first, then add integration coverage where behavior crosses modules or external boundaries. Use names that describe behavior, such as `client_returns_cached_response` or `renders_empty_state_when_no_items_exist`. Keep fixtures local to the test area that uses them.

## Commit & Pull Request Guidelines
No local Git history is available yet, so there is no repository-specific commit pattern to follow. Once version control is initialized, use short imperative subjects and keep commits focused; `feat: add session bootstrap` and `fix: handle empty config` are good starting points. Pull requests should describe scope, testing performed, linked issues, and any screenshots or sample output needed to review UI or CLI changes.

## Security & Configuration Tips
Do not commit secrets, personal tokens, or machine-specific configuration. Store local overrides in ignored environment files such as `.env.local`, and provide safe defaults or sample values in tracked templates.
