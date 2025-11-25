---
description: Create a bug fix plan in specs/*.md
---
# Bug Planning

Create a plan in `specs/*.md` to resolve the `Bug` using the `Plan Format` below.

## Instructions

- Research the codebase to understand and reproduce the bug
- Be surgical - minimal changes to fix the root cause
- Create the plan in `specs/<bug-name>.md`
- Replace all `<placeholder>` values with specific details

## Relevant Files

Focus on these directories based on bug location:

**Frontend Bugs (apps/web/):**

- `app/` - Next.js routes and pages
- `components/` - React components (dashboard/, onboarding/, ask-gist/, ui/)
- `hooks/` - Custom hooks
- `lib/` - Utilities and state
- `types/` - TypeScript definitions

**Backend Bugs (apps/web/):**

- `convex/` - Database schema and functions

**AI Bugs (packages/ai/):**

- `agents/` - AI agent implementations
- `engines/` - Data fetching engines

**Styling Bugs (apps/web/):**

- `app/globals.css` - Global styles
- `components/ui/` - shadcn components

## Plan Format

````md
# Bug: <bug name>

## Description

<describe the bug - expected vs actual behavior>

## Steps to Reproduce

1. <step>
2. <step>
3. <step>

## Root Cause

<explain why the bug occurs>

## Solution

<describe the fix approach>

## Relevant Files

### Files to Modify

<list files that need changes and why>

## Step by Step Tasks

### 1. <Task Name>

- <subtask>

### 2. <Task Name>

- <subtask>

<continue as needed>

## Validation Commands

```bash
bun run build                    # Build all workspaces
bun run lint                     # Lint all workspaces
cd apps/web && bun run test      # Run tests
# Manual: <steps to verify the fix>
```
````

## Notes

<additional context if needed>
```

## Bug

$ARGUMENTS

## Report

After creating the plan:

- Summarize the bug and fix
- Include path to the plan file: `specs/<bug-name>.md`
