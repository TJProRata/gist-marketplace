---
description: Create a chore plan in specs/*.md
---
# Chore Planning

Create a plan in `specs/*.md` to resolve the `Chore` using the `Plan Format` below.

## Instructions

- Research the codebase to understand what needs to change
- Create the plan in `specs/<chore-name>.md`
- Replace all `<placeholder>` values with specific details
- Be thorough - chores should be done right the first time

## Relevant Files

Focus on these directories based on chore type:

**Code Cleanup / Refactoring (apps/web/):**

- `components/` - React components (dashboard/, onboarding/, ask-gist/, ui/)
- `lib/` - Utilities and state
- `hooks/` - Custom hooks
- `types/` - TypeScript definitions

**AI Package Cleanup (packages/ai/):**

- `agents/` - AI agents
- `agent-architectures/` - Patterns
- `engines/` - Data fetching

**Configuration / Tooling:**

- `package.json` - Root workspace + catalog dependencies
- `apps/web/package.json` - Web app dependencies
- `packages/ai/package.json` - AI package dependencies
- `tsconfig.json` - Root TypeScript config
- `apps/web/tsconfig.json` - Web app TypeScript config

**Documentation:**

- `README.md` - Project overview
- `CLAUDE.md` - Comprehensive project documentation

**Backend (apps/web/):**

- `convex/` - Database schema and functions

## Plan Format

````md
# Chore: <chore name>

## Description

<describe the chore and why it's needed>

## Relevant Files

### Files to Modify

<list files that need changes and why>

### Files to Create (if any)

<list new files needed>

## Step by Step Tasks

### 1. <Task Name>

- <subtask>
- <subtask>

### 2. <Task Name>

- <subtask>
- <subtask>

<continue as needed>

## Validation Commands

```bash
bun run build                    # Build all workspaces
bun run lint                     # Lint all workspaces
cd apps/web && bun run test      # Run tests (if applicable)
```
````

## Notes

<additional context if needed>
```

## Chore

$ARGUMENTS

## Report

After creating the plan:

- Summarize the chore
- Include path to the plan file: `specs/<chore-name>.md`
