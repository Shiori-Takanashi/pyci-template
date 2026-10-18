# Python-CI-Templates

Python-CI-Template is a template for local code quality checks and CI with GitHub Actions.

## Tool Versions

This template uses the following tool versions:

| Tool | Version |
| --- | --- |
| uv | 0.13.* |
| ruff | 0.17.* |

## Commands (Not yet implemented)

The `Justfile` provides useful shortcuts for linting, formatting, type checking, testing, and installing Git hooks.

## Git Hooks

Git hooks are installed using `pre-commit` and configured in `.pre-commit-config.yaml`. The hooks use the settings defined in `pyproject.toml` for `ruff`, `mypy`, and `pytest`.

## GitHub Actions (Not yet implemented)

The CI workflow is configured in `ci.yml`. It uses local hooks rather than mirror repositories to keep checks consistent between local development and CI.

### Example Recipes (Not yet implemented)

```just
ruff-modify: ruff-lint ruff-format

ruff-lint:
    uv run ruff check --fix {{TARGETS}}

ruff-format:
    uv run ruff format {{TARGETS}}
```
