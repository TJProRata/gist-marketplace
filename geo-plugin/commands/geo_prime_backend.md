---
allowed-tools: Bash, Read
description: Context for Convex backend work
---
# Convex Backend Context

## Run

```bash
git status --short
```

## Read
- docs/convexdocs/convex_database.md
- docs/convexdocs/convex_functions.md
- convex/schema.ts
- convex/signups.ts
- convex/contentBriefs.ts

## Key Patterns
- Tables: signups, contentBriefs
- All tables use indexes for efficient queries
- Mutations return { success, duplicate? } for UX-friendly handling
- Dev: `bunx convex dev` | Prod: `npx convex deploy --yes`

ARGUMENTS: $ARGUMENTS
