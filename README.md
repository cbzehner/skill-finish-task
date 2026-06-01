# Finish Task

Finish coding work end-to-end after implementation is believed complete: validate evidence, review the diff, use magi/counsel and complexity-guard, check architecture/philosophy alignment, capture or attach screenshots for UI work, then deliver through a PR, guarded default-branch commit, or worktree merge based on repository metadata. Use when the user says finish, wrap up, ship it, make a PR, create/update the PR, merge this worktree into the default branch, commit directly to the default branch, or asks for a task completion flow.

## Skill

This repository packages one portable agent skill:

- `finish-task` - Finish coding work end-to-end after implementation is believed complete: validate evidence, review the diff, use magi/counsel and complexity-guard, check architecture/philosophy alignment, capture or attach screenshots for UI work, then deliver through a PR, guarded default-branch commit, or worktree merge based on repository metadata. Use when the user says finish, wrap up, ship it, make a PR, create/update the PR, merge this worktree into the default branch, commit directly to the default branch, or asks for a task completion flow.

The canonical skill body lives at `skills/finish-task/SKILL.md`. Keep behavior changes there; keep this README focused on installation and packaging.

## Install

Clone the repository, then run the installer:

```bash
git clone https://github.com/cbzehner/skill-finish-task.git
cd skill-finish-task
./install.sh all
```

Install targets:

- `./install.sh claude` -> `~/.claude/skills/finish-task`
- `./install.sh codex` -> `~/.codex/skills/finish-task`
- `./install.sh agents` -> `~/.agents/skills/finish-task` for generic agent harnesses such as Pi/Hermes-style setups
- `./install.sh opencode` -> `~/.config/opencode/skills/finish-task`
- `./install.sh all --copy` copies files instead of symlinking

Manual installation is just a symlink or copy from `skills/finish-task` into your agent's skills directory.

## Compatibility

This repo uses the common `skills/<name>/SKILL.md` layout so agents that understand file-based skills can load it directly. Host-specific metadata is included where useful:

- Claude Code: `.claude-plugin/plugin.json` and direct `~/.claude/skills` install
- Codex CLI: `.codex-plugin/plugin.json` with `skills: "./skills/"` and direct `~/.codex/skills` install
- Other agents: direct install to the agent's skills directory; unsupported frontmatter fields can be ignored

Some skills mention optional host tools such as `Task`, `Agent`, `Skill`, MCP tools, or browser automation CLIs. On hosts that do not provide those tools, adapt to equivalent local capabilities and keep the same workflow intent.

## Public Safety

These repositories are public. Do not commit organization-specific instructions, private repository names, secrets, tokens, cookies, raw session logs, customer data, or machine-local paths. Use environment variables and generic paths in examples.

## Repository Layout

```text
.claude-plugin/plugin.json   # Claude plugin metadata
.codex-plugin/plugin.json    # Codex plugin metadata
install.sh                   # Symlink/copy installer for common agent skill dirs
skills/finish-task/SKILL.md
README.md
LICENSE
```

## License

MIT
