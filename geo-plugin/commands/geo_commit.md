---
description: Create a commit with conventional commit format
---
# Git Commit

Create a commit with conventional commit format.

## Run

```bash
git status
git diff --staged
git add -A
git commit -m "<type>: <description>"
```

## Instructions

Commit message format: `<type>: <description>`

Types:

- `feat` - New feature
- `fix` - Bug fix
- `chore` - Maintenance
- `refactor` - Code refactoring
- `docs` - Documentation
- `style` - Formatting (no code change)

Rules:

- Present tense ("add" not "added")
- 50 chars or less
- No period at end
- Lowercase

Examples:

- `feat: add dark mode toggle to dashboard`
- `fix: resolve sidebar collapse on mobile`
- `chore: update convex schema indexes`

## Input

$ARGUMENTS

## Report

Return the commit message used.
