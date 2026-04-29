---
name: feature-or-bugfix-with-unit-tests
description: Workflow command scaffold for feature-or-bugfix-with-unit-tests in skyvern.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /feature-or-bugfix-with-unit-tests

Use this workflow when working on **feature-or-bugfix-with-unit-tests** in `skyvern`.

## Goal

Implements a new feature or fixes a bug in backend code, accompanied by new or updated unit tests to verify the change.

## Common Files

- `skyvern/cli/mcp_tools/__init__.py`
- `skyvern/cli/commands/__init__.py`
- `skyvern/cli/mcp_tools/_validation.py`
- `skyvern/cli/mcp_tools/schedule.py`
- `skyvern/cli/schedule_command.py`
- `skyvern/forge/agent_functions.py`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Modify or add backend implementation files (e.g., Python modules in skyvern/cli, skyvern/forge, skyvern/)
- Add or update corresponding unit test files in tests/unit/

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.