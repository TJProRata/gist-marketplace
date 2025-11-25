---
allowed-tools: Bash, Read
description: Context for onboarding flow work
---
# Onboarding Flow Context

## Run

```bash
git status --short
ls apps/web/app/onboarding/
ls apps/web/components/onboarding/
```

## Read
- apps/web/app/onboarding/layout.tsx
- apps/web/lib/onboarding-state.ts
- apps/web/components/onboarding/onboarding-layout.tsx
- apps/web/types/onboarding.types.ts

## Onboarding Routes

```
apps/web/app/onboarding/
├── layout.tsx          # Minimal onboarding layout
├── auth/               # Authentication step
├── brand-setup/        # Brand configuration
├── goals/              # Goal selection
├── topics/             # Topic selection
├── prompts/            # Prompt configuration
├── plan/               # Plan selection
├── loading/            # Processing state
└── performance/        # Results display
```

## Onboarding Components

```
apps/web/components/onboarding/
├── onboarding-layout.tsx    # Split-screen layout
├── split-screen-layout.tsx  # Left/right panels
├── left-panel.tsx           # Content panel
├── right-panel.tsx          # Visual panel
├── progress-header.tsx      # Step progress
├── goal-card.tsx            # Goal selection cards
├── topic-chip.tsx           # Topic pills
├── topic-item.tsx           # Topic list items
├── pricing-card.tsx         # Plan cards
├── help-button.tsx          # Help overlay
└── onboarding-widget.tsx    # Embedded widget
```

## State Flow
```
auth → brand-setup → goals → topics → prompts → plan → loading → performance
```

## State Management
- `lib/onboarding-state.ts` - Multi-step wizard state
- Types: `types/onboarding.types.ts`

ARGUMENTS: $ARGUMENTS
