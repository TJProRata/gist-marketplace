---
allowed-tools: Bash, Read
description: Context for dashboard pages and features
---
# Dashboard Development Context

## Run

```bash
git status --short
ls apps/web/app/dashboard/
ls apps/web/components/dashboard/ | head -20
```

## Read
- apps/web/app/dashboard/layout.tsx
- apps/web/app/dashboard/page.tsx
- apps/web/components/dashboard/dashboard-client.tsx
- apps/web/lib/dashboard-state.ts

## Dashboard Routes

```
apps/web/app/dashboard/
├── layout.tsx          # Dashboard layout with sidebar
├── page.tsx            # Main dashboard (DashboardClient)
├── loading.tsx         # Loading state
├── analytics/          # Analytics page
├── brands/             # Brand management
├── content/            # Content management
├── insights/           # Insights page
└── products/           # Product management
```

## Key Components (43 total)

| Component | Purpose |
|-----------|---------|
| dashboard-client.tsx | Main dashboard container |
| dashboard-grid.tsx | Grid layout |
| dashboard-header.tsx | Header with actions |
| sidebar.tsx | Navigation sidebar |
| brand-selector.tsx | Brand picker |
| action-item.tsx | Action cards |
| metrics-panel.tsx | Metrics display |

## State Management
- `lib/dashboard-state.ts` - Sidebar state (localStorage)
- Navigation: overview, analytics, content, brands, products, insights
- Layout: Collapsible sidebar + main content area
- Mobile: Hamburger menu with sheet overlay

## Related Types
- `apps/web/types/dashboard.types.ts` - Dashboard type definitions

ARGUMENTS: $ARGUMENTS
