---
description: Create a feature plan in specs/*.md
---
# Feature Planning

Create a plan in `specs/*.md` to implement the `Feature` using the `Plan Format` below.

## Instructions

- Research the codebase to understand existing patterns before planning
- Use CVA variants for any new components (see `apps/web/components/ui/button.tsx`)
- Follow existing file organization conventions
- Create the plan in `specs/<feature-name>.md`
- Replace all `<placeholder>` values with specific details
- Use `--think-hard` flag for complex features

## Relevant Files

Focus on these directories based on feature type:

**Frontend Features (apps/web/):**

- `app/` - Next.js routes and pages
- `components/` - React components (ui/, shared/, dashboard/, ask-gist/, onboarding/)
- `hooks/` - Custom React hooks (use-chat-stream, use-content-flow, etc.)
- `lib/` - Utilities, state management, mock data
- `types/` - TypeScript definitions

**Backend Features (apps/web/):**

- `convex/schema.ts` - Database schema (10+ tables)
- `convex/*.ts` - Mutations and queries

**AI Features (packages/ai/):**

- `agents/` - AI agents with agent-critic pattern
- `agent-architectures/` - Reusable patterns
- `engines/` - Data fetching (AI Overview)

**Styling (apps/web/):**

- `app/globals.css` - Global styles, CSS variables
- shadcn/ui components in `components/ui/`

## Plan Format

````md
# Feature: <feature name>

## Description

<describe the feature, its purpose, and value to users>

## User Story

As a <user type>
I want to <action>
So that <benefit>

## Relevant Files

### Existing Files to Modify

<list files that need changes and why>

### New Files to Create

<list new files needed>

## Implementation Plan

### Phase 1: Foundation

<foundational work - types, schema changes, utilities>

### Phase 2: Core Implementation

<main feature implementation>

### Phase 3: Integration

<connecting pieces, testing, polish>

## Step by Step Tasks

### 1. <Task Name>

- <subtask>
- <subtask>

### 2. <Task Name>

- <subtask>
- <subtask>

<continue as needed>

## Testing Strategy

- <how to test the feature>
- <edge cases to consider>

## Acceptance Criteria

- [ ] <specific, measurable criterion>
- [ ] <specific, measurable criterion>

## Validation Commands

```bash
bun run build                    # Build all workspaces
bun run lint                     # Lint all workspaces
cd apps/web && bunx convex dev   # Test Convex functions (if backend changes)
cd apps/web && bun run test      # Run tests
```
````

## Notes

<additional context, future considerations, dependencies>

```

## Feature
$ARGUMENTS

## Report
After creating the plan:
- Summarize what you planned
- Include path to the plan file: `specs/<feature-name>.md`
```
