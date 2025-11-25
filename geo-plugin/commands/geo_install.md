# Install & Setup

## Read

- .env.sample

## Run

```bash
# Install dependencies
bun install

# Copy environment file
cp .env.sample .env.local
```

## Report

- Confirm dependencies installed
- Instruct user to:
  1. Get Convex URL: Run `bunx convex dev` to create/connect project
  2. Update `.env.local` with `NEXT_PUBLIC_CONVEX_URL` from Convex dashboard
  3. Start dev server: `bun run dev`
