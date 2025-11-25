---
allowed-tools: Bash, Read
description: Context for creating shadcn-style components
---
# Component Development Context

## Run

```bash
git status --short
```

## Read
- docs/dashboard_building_protocol.md
- docs/shadcn/shadcn_component_library_bp.md
- docs/shadcn/variants.md
- components/ui/button.tsx
- components/dashboard/action-item.tsx

## Key Patterns
- CVA variants with `cva()` from class-variance-authority
- React.forwardRef for ref forwarding
- TypeScript props extending `VariantProps<typeof variants>`
- Use `cn()` to merge variant classes with custom className

ARGUMENTS: $ARGUMENTS
