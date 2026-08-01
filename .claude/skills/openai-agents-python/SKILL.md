```markdown
# openai-agents-python Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns, coding conventions, and collaborative workflows used in the `openai-agents-python` repository. You'll learn how to structure code, write and organize commits, update documentation, manage releases, and write tests in line with the project's standards.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `agentRunner.py`, `dataLoader.py`

### Import Style
- Prefer **relative imports** within the package.
  - Example:
    ```python
    from .utils import parseConfig
    from ..core.agent import Agent
    ```

### Export Style
- Use **named exports** (explicitly listing what the module exports).
  - Example:
    ```python
    __all__ = ["Agent", "AgentRunner"]
    ```

### Commit Messages
- Follow **conventional commit** patterns with these prefixes:
  - `docs:` for documentation changes
  - `fix:` for bug fixes
  - `chore:` for maintenance tasks
- Keep commit messages concise (average 38 characters).
  - Example: `docs: update README with usage example`

## Workflows

### Documentation Update
**Trigger:** When you want to update, improve, or translate documentation.  
**Command:** `/update-docs`

1. Edit one or more files in the `docs/` directory and/or `README.md`.
2. Optionally, update `mkdocs.yml` or other documentation configuration files.
3. Commit your changes with a message starting with `docs:`.
   - Example: `docs: add API usage section`
4. Open a pull request for review.

**Files Involved:**
- `docs/*.md`
- `docs/**/index.md`
- `README.md`
- `mkdocs.yml`

### Version Bump
**Trigger:** When you want to release a new version of the project.  
**Command:** `/bump-version`

1. Update the version number in `pyproject.toml`.
   - Example:
     ```toml
     [project]
     version = "1.2.0"
     ```
2. Update `uv.lock` or other lock files as needed.
3. Commit your changes with a message like `Bump version to 1.2.0`.
4. Open a pull request for review and merge to release.

**Files Involved:**
- `pyproject.toml`
- `uv.lock`

## Testing Patterns

- Test files follow the pattern: `*.test.*` (e.g., `agentRunner.test.py`).
- The specific testing framework is not enforced or detected.
- To write a test, create a file named with `.test.` and use standard Python testing practices.
  - Example:
    ```python
    # agentRunner.test.py
    def test_agent_runs():
        agent = AgentRunner()
        assert agent.run() is True
    ```

## Commands

| Command        | Purpose                                   |
|----------------|-------------------------------------------|
| /update-docs   | Start a documentation update workflow     |
| /bump-version  | Start a version bump and release workflow |
```
