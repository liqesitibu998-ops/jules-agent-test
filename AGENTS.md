# Agent Instructions

This repository may be edited by Jules through GitHub Actions.

## Main Rules

- Work through Pull Requests.
- Keep changes small enough to review.
- Do not touch production secrets.
- Do not add credentials to the repository.
- Do not modify deployment files unless the selected task explicitly requires it.
- Preserve existing behavior unless the task asks to change it.
- Add or update tests when code behavior changes.

## Task Queue

If `agent_tasks.json` exists:

1. Read it first.
2. Choose the first task with `"status": "todo"`.
3. Respect `allowed_paths`.
4. Implement the acceptance criteria.
5. Set the completed task to `"done"`.
6. Add 1-3 new safe `"todo"` tasks if useful.

If `agent_tasks.json` does not exist:

1. Inspect the repository.
2. Choose one low-risk improvement.
3. Create a Pull Request.
