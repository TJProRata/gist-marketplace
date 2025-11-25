---
description: Install and setup Gist GEO monorepo
---
# Install & Setup

## Read

- apps/web/.env.sample

## Run

```bash
# Install all workspace dependencies (from root)
bun install

# Copy environment file
cp apps/web/.env.sample apps/web/.env.local
```

## Environment Variables Required

```bash
# Clerk Authentication
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=pk_test_...
CLERK_SECRET_KEY=sk_test_...
CLERK_JWT_ISSUER_DOMAIN=https://your-domain.clerk.accounts.dev

# Convex Database (from Convex dashboard)
CONVEX_DEPLOYMENT=...
NEXT_PUBLIC_CONVEX_URL=...

# SerpAPI (for AI Overview engine)
SERPAPI_API_KEY=...

# OpenAI (for AI agents)
OPENAI_API_KEY=...
```

## Report

- Confirm dependencies installed
- Instruct user to:
  1. Edit `apps/web/.env.local` with Clerk keys from dashboard
  2. Run `cd apps/web && bunx convex dev` to create/connect Convex project
  3. Add Convex URL from dashboard to `.env.local`
  4. Start dev servers: `bun run dev` (from root)
