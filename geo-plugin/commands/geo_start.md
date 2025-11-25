---
description: Start Gist GEO dev servers
---
# Start Dev Servers

## Run

```bash
# Kill any process on port 3000
lsof -ti:3000 | xargs kill -9 2>/dev/null || true

# From repository root - starts all workspaces
bun run dev
```

## Alternative: Run Separately

```bash
# Terminal 1: Start Convex dev server
cd apps/web && bunx convex dev

# Terminal 2: Start Next.js dev server (from root)
bun run dev
```

## Ports
- **Next.js**: http://localhost:3000
- **Convex**: Dashboard at https://dashboard.convex.dev

## Workspaces
- `apps/web` - Next.js 16 application
- `packages/ai` - AI agents package (no dev server)

Open http://localhost:3000
