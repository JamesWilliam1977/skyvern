```markdown
# skyvern Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill introduces the core development patterns and workflows used in the `skyvern` Python codebase. It covers coding conventions, commit styles, and the process for contributing new features or bug fixes with accompanying unit tests. The repository is organized with clear module separation and emphasizes maintainable, testable code.

## Coding Conventions

- **File Naming:**  
  All Python files use `snake_case` naming for consistency.  
  *Example:*  
  ```
  skyvern/cli/mcp_tools/schedule.py
  ```

- **Import Style:**  
  Imports use aliases to clarify usage and avoid naming conflicts.  
  *Example:*  
  ```python
  import skyvern.forge.agent_functions as agent_funcs
  ```

- **Export Style:**  
  Modules use named exports, explicitly listing public objects.  
  *Example (`__init__.py`):*  
  ```python
  from .schedule import ScheduleManager

  __all__ = ["ScheduleManager"]
  ```

- **Commit Messages:**  
  Follows [Conventional Commits](https://www.conventionalcommits.org/) with prefixes like `fix:` and `feat:`.  
  *Example:*  
  ```
  feat: add schedule validation for overlapping events
  ```

## Workflows

### Feature or Bugfix with Unit Tests
**Trigger:** When you want to add a new backend feature or fix a bug and ensure it is tested.  
**Command:** `/feature-with-tests`

1. **Modify or add implementation files:**  
   Update or create Python modules in relevant directories, such as `skyvern/cli/`, `skyvern/forge/`, or the root `skyvern/` package.
   *Example:*  
   ```
   skyvern/cli/mcp_tools/_validation.py
   skyvern/forge/agent_functions.py
   ```
2. **Add or update unit tests:**  
   Create or update corresponding test files in `tests/unit/` to cover your changes.
   *Example:*  
   ```
   tests/unit/test_schedule_cli.py
   tests/unit/test_exception_messages.py
   ```
3. **Follow coding conventions:**  
   Use snake_case for files, alias imports, and named exports.
4. **Write a conventional commit message:**  
   Use `feat:` for new features or `fix:` for bug fixes.
5. **Submit your changes for review.**

## Testing Patterns

- **Test Framework:**  
  The exact framework is unknown, but test files follow the pattern `*.test.ts`.  
  *Note:* Despite the `.ts` (TypeScript) pattern, Python unit tests are present in `tests/unit/`.
- **Test File Organization:**  
  Unit tests reside in `tests/unit/` and are named according to the module they test.
  *Example:*  
  ```
  tests/unit/test_mcp_tool_titles.py
  ```
- **Test Coverage:**  
  Every feature or bugfix should be accompanied by new or updated unit tests.

## Commands

| Command              | Purpose                                                        |
|----------------------|----------------------------------------------------------------|
| /feature-with-tests  | Start a feature or bugfix workflow with accompanying unit tests |
```
