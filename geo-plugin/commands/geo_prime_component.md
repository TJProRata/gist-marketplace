---
allowed-tools: Bash, Read
description: Context for creating shadcn-style components
---
# Component Development Context

## Run

```bash
git status --short
ls apps/web/components/ui/ | head -20
```

## Read
- apps/web/components/ui/button.tsx
- apps/web/components/dashboard/action-item.tsx
- apps/web/components/shared/
- apps/web/lib/utils.ts

## Component Organization

```
apps/web/components/
├── ui/              # 55+ shadcn/ui components (New York style)
├── dashboard/       # 43 dashboard-specific components
├── onboarding/      # 11 onboarding flow components
├── shared/          # 17 shared components
├── ask-gist/        # 12 AI chat components
├── chat/            # Chat interface components
├── app/             # App-level (header, footer, providers)
├── auth/            # Clerk auth components
└── convex/          # Convex client provider
```

## shadcn/ui Configuration
- Style: "new-york"
- Base color: neutral
- CSS variables enabled
- Config: `apps/web/components.json`

## Key Patterns

### CVA Variants
```tsx
import { cva, type VariantProps } from "class-variance-authority"
import { cn } from "@/lib/utils"

const buttonVariants = cva("base-classes", {
  variants: {
    variant: { default: "...", secondary: "..." },
    size: { default: "...", sm: "...", lg: "..." }
  },
  defaultVariants: { variant: "default", size: "default" }
})

interface ButtonProps extends VariantProps<typeof buttonVariants> {}
```

### forwardRef Pattern
```tsx
const Button = React.forwardRef<HTMLButtonElement, ButtonProps>(
  ({ className, variant, size, ...props }, ref) => (
    <button
      className={cn(buttonVariants({ variant, size, className }))}
      ref={ref}
      {...props}
    />
  )
)
Button.displayName = "Button"
```

## Path Aliases
- `@/*` → `apps/web/*`
- `@/ui` → `components/ui/`
- `@/lib` → `lib/`
- `@/hooks` → `hooks/`

ARGUMENTS: $ARGUMENTS
