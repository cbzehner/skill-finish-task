# Finish Task

Finish coding work with review gates, visual evidence, and repo-appropriate delivery.

The skill is meant for the end of a task, when the agent should stop coding and prove the work is ready. It is project-neutral: it should work in any Git repository under `~/Developer/*/*` by detecting remotes, forks, upstreams, default branches, and local project instructions instead of hard-coded repo names.

## What It Does

- Reviews the complete diff before delivery
- Runs local verification and records exact commands
- Uses `magi` for a second-opinion review
- Applies `complexity-guard`
- Checks architecture and repo philosophy files
- Captures screenshots for UI changes
- Uploads screenshots to GitHub user attachments only after explicit public-URL consent
- Creates or updates PRs when the repo should be reviewed through a branch
- Commits or merges into the default branch only for local/user-owned repos or when explicitly requested

## Usage

Ask the agent to finish the task:

```text
finish this task
wrap this up and make a PR
finish and merge this local worktree into the default branch
ship this on the default branch
```

## Files

```text
.claude-plugin/plugin.json
.codex-plugin/plugin.json
skills/finish-task/SKILL.md
skills/finish-task/recipes/review-gates.md
skills/finish-task/recipes/visual-evidence.md
skills/finish-task/recipes/delivery.md
```

## Packaging Notes

This follows the same `~/Developer/Personal/skill-*` layout as the other stable local skills:

- `.claude-plugin/plugin.json` for Claude plugin installs
- `.codex-plugin/plugin.json` with `skills: "./skills/"` for Codex plugin installs
- one skill directory under `skills/`
- small recipe files only where they remove noise from the main trigger file

Project-specific helpers belong in the target repo. This skill can reference them when present, but should not require or recreate them.

## License

MIT
