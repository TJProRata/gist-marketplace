# Chore Planning

Create a plan in `specs/*.md` to resolve the `Chore` using the `Plan Format` below.

## Instructions

- Research the codebase to understand what needs to change
- Create the plan in `specs/<chore-name>.md`
- Replace all `<placeholder>` values with specific details
- Be thorough - chores should be done right the first time

## Relevant Files

Focus on these directories based on chore type:

**Code Cleanup / Refactoring:**

- `components/` - React components
- `lib/` - Utilities and state
- `hooks/` - Custom hooks

**Configuration / Tooling:**

- `package.json` - Dependencies and scripts
- `tsconfig.json` - TypeScript config
- `tailwind.config.ts` - Tailwind config
- `vercel.json` - Deployment config

**Documentation:**

- `README.md` - Project overview
- `doc/` - Project documentation
- `docs/` - Technical documentation

**Backend:**

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
bun run build          # Verify no build errors
bun run lint           # Check for lint issues
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
