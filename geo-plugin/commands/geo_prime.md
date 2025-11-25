---
allowed-tools: Bash, Read
description: Quick project state check for Gist GEO monorepo
---
# Gist GEO - Project State

## Run

```bash
git log --oneline -5
git status --short
```

## Read
- CLAUDE.md
- README.md

## Project Structure

Bun workspace monorepo:
- `apps/web/` - Next.js 16 web application
- `packages/ai/` - Shared AI agents and utilities (@gist-geo/ai)

## Key Paths

| Area | Path |
|------|------|
| App Routes | `apps/web/app/` |
| Components | `apps/web/components/` |
| Database | `apps/web/convex/` |
| Hooks | `apps/web/hooks/` |
| Types | `apps/web/types/` |
| AI Agents | `packages/ai/agents/` |
| AI Engines | `packages/ai/engines/` |

ARGUMENTS: $ARGUMENTS
