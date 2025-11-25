---
allowed-tools: Bash, Read
description: Context for onboarding flow work
---
# Onboarding Flow Context

## Run

```bash
git status --short
ls -1 app/onboarding-preview/flow/
```

## Read
- lib/onboarding-state.ts
- app/onboarding-preview/flow/auth/page.tsx

## Key Patterns
- Multi-step wizard with split-screen layout
- State machine: auth → brand-setup → goals → topics → prompts → plan → loading → performance
- OnboardingLayout component for consistent structure

ARGUMENTS: $ARGUMENTS
