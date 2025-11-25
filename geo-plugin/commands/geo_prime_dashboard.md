---
allowed-tools: Bash, Read
description: Context for dashboard pages and features
---
# Dashboard Development Context

## Run

```bash
git status --short
ls -1 components/dashboard/
```

## Read
- docs/dashboard_building_protocol.md
- docs/gist_geo/gist_geo_style_guide.md
- app/dashboard/layout.tsx
- app/dashboard/page.tsx
- lib/dashboard-state.ts

## Key Patterns
- Sidebar state persisted to localStorage
- Navigation: overview, agent-analytics, content, brands, products, insights
- Layout: Sidebar + main content area with mobile hamburger menu

ARGUMENTS: $ARGUMENTS
