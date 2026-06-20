# Jules GitHub Actions Loop

**Note: This repository is a Jules automation test.**

This package implements the same basic loop described in the post:

1. Jules creates a Pull Request.
2. GitHub Actions runs tests.
3. If tests pass, the PR is merged.
4. After merge, another workflow triggers Jules again.
5. Jules takes the next task and creates the next Pull Request.

## Files

- `.github/workflows/jules_automerge.yml`
- `.github/workflows/jules_next_task.yml`
- `AGENTS.md`
- `agent_tasks.json`

## Required GitHub Secrets

Add these in GitHub:

Repository → Settings → Secrets and variables → Actions → New repository secret

Required:

- `JULES_API_KEY`
- `PAT`

`PAT` is a GitHub classic token with permissions for repository contents and pull requests. If the workflow needs to edit workflows, it also needs workflow permission.

## Required Jules Setup

1. Open Jules.
2. Connect GitHub.
3. Give Jules access to the target repository.
4. Create a Jules API key.
5. Save it as `JULES_API_KEY` in GitHub Actions secrets.

## How To Start

1. Copy these files into the root of your GitHub repository.
2. Commit and push.
3. Open GitHub → Actions.
4. Run workflow:

`2. Trigger Next Jules Task`

The loop starts after the first Jules PR is merged.

## Important

This version includes auto-merge, exactly like the described loop. That means successful Jules PRs can be merged without manual review.
