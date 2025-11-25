---
description: Push branch and create PR to main
---
# Create Pull Request

Push branch and create PR to main.

## Run

```bash
# Check what will be in the PR
git log origin/main..HEAD --oneline
git diff origin/main...HEAD --stat

# Push and create PR
git push -u origin $(git branch --show-current)
gh pr create --title "<title>" --body "<body>" --base main
```

## Instructions

PR Title format: `<type>: <description>`

- Same format as commit messages

PR Body template:

```md
## Summary

<1-2 sentence description>

## Changes

- <change 1>
- <change 2>

## Testing

- [ ] `bun run build` passes
- [ ] `bun run lint` passes
- [ ] Manual testing completed
```

## Input

$ARGUMENTS

## Report

Return the PR URL.
