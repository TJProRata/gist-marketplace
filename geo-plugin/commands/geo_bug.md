# Bug Planning

Create a plan in `specs/*.md` to resolve the `Bug` using the `Plan Format` below.

## Instructions

- Research the codebase to understand and reproduce the bug
- Be surgical - minimal changes to fix the root cause
- Create the plan in `specs/<bug-name>.md`
- Replace all `<placeholder>` values with specific details

## Relevant Files

Focus on these directories based on bug location:

**Frontend Bugs:**

- `app/` - Next.js routes and pages
- `components/` - React components
- `hooks/` - Custom hooks
- `lib/` - Utilities and state

**Backend Bugs:**

- `convex/` - Database schema and functions

**Styling Bugs:**

- `app/globals.css` - Global styles
- `tailwind.config.ts` - Tailwind config

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
bun run build          # Verify no build errors
bun run lint           # Check for lint issues
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
