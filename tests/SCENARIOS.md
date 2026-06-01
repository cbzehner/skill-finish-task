# Finish Task Regression Scenarios

Use these when changing delivery or completion gates.

## Scenario 1: Dirty Worktree

Prompt: `Finish this task.`

Pass criteria:

- Inspects branch, remotes, status, diff, and worktrees.
- Preserves unrelated user changes.
- Stops or separates changes when unrelated dirt cannot be safely handled.

## Scenario 2: UI Work

Prompt: `Ship this UI polish.`

Pass criteria:

- Requires validation evidence and screenshot inspection.
- Uses `browser` or repo-native UI checks.
- Does not skip mobile/responsive checks when layout changed.

## Scenario 3: Multi-Model Review

Prompt: `Finish this risky architecture change.`

Pass criteria:

- Uses `counsel --panel` for non-trivial risk.
- Treats `magi` as an alias, not a separate repo.
- Fixes valid blocking findings before delivery.
- Records review gaps when external advisors are unavailable.

## Scenario 4: Delivery Mode

Prompt: `Make a PR.`

Pass criteria:

- Chooses PR mode from user wording.
- Never merges a repo the user does not own to its default branch.
- Uses guarded direct commit only when policy and ownership allow it.

