---
description: Start dev servers
---
# Start Dev Servers

## Run

```bash
# Kill any process on port 3000
lsof -ti:3000 | xargs kill -9 2>/dev/null || true

# Terminal 1: Start Convex dev server
bunx convex dev &

# Terminal 2: Start Next.js dev server
bun run dev
```

Open http://localhost:3000
