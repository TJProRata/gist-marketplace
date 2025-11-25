---
description: Create a new branch from main
---
# Create Feature Branch

Create a new branch from main for the given feature/fix.

## Run

```bash
git checkout main
git pull origin main
git checkout -b <branch_name>
```

## Instructions

Generate branch name in format: `<type>/<short-description>`

Types:

- `feat/` - New feature
- `fix/` - Bug fix
- `chore/` - Maintenance task
- `refactor/` - Code refactoring

Examples:

- `feat/add-dark-mode`
- `fix/dashboard-sidebar-collapse`
- `chore/update-dependencies`

## Input

$ARGUMENTS

## Report

Return the branch name created.
