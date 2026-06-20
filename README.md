# jules-agent-test

## Project Structure

This repository is primarily a documentation and task queue project.

- **`.github/`**: Contains GitHub Actions workflows, such as `.github/workflows/agent-loop.yml`, which automates task execution.
- **`AGENTS.md`**: Outlines instructions and rules for agents modifying this repository (e.g., keeping changes small, working via PRs).
- **`agent_tasks.json`**: The main task queue file, tracking the status of `"todo"` and `"done"` items.
- **`README.md`**: This file, providing an overview of the project structure.
- **`README_INSTALL.md`**: Details any installation or setup instructions.

## Testing Philosophy

This repository is primarily a documentation and task queue project, so it currently lacks traditional test suites (no unit, integration, or end-to-end tests exist).

However, any future code behavior changes should be accompanied by appropriate tests to ensure stability and verify functionality.
