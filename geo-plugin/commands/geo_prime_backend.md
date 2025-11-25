---
allowed-tools: Bash, Read
description: Context for Convex backend work
---
# Convex Backend Context

## Run

```bash
git status --short
ls apps/web/convex/
```

## Read
- apps/web/convex/schema.ts
- apps/web/convex/signups.ts
- apps/web/convex/contentBriefs.ts
- apps/web/convex/products.ts
- apps/web/convex/mentions.ts

## Database Schema

| Table | Purpose |
|-------|---------|
| users | Clerk auth integration (externalId) |
| brands | Top-level entities with productIds[] |
| products | Brand products with value_props, icps, iab_cat |
| queries | Research queries for products |
| topics | Product research topics |
| query_runs | Query execution results per provider |
| providers | chatgpt, google, ai_overview, claude, gemini |
| justifications | Product justifications with citations |
| coverages | Query coverage scores |
| scores | Aggregated GEO metrics (SOV, EMC, JUST, COVER) |
| mentions | Product mentions from query runs |
| signups | Email signups |
| contentBriefs | Content planning documents |

## Convex Functions

| File | Purpose |
|------|---------|
| schema.ts | Table definitions |
| products.ts | Product CRUD |
| mentions.ts | Mention extraction |
| signups.ts | Email signup handling |
| contentBriefs.ts | Content brief management |
| review.ts | Review workflow |
| justifications.ts | Justification scoring |

## Key Commands
- Dev: `cd apps/web && bunx convex dev`
- Deploy: `cd apps/web && bunx convex deploy`

ARGUMENTS: $ARGUMENTS
