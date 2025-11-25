---
allowed-tools: Bash, Read
description: Context for Ask Gist AI chat interface
---
# Ask Gist Chat Context

## Run

```bash
git status --short
ls apps/web/components/ask-gist/
```

## Read
- apps/web/components/ask-gist/ask-gist-chat.tsx
- apps/web/components/ask-gist/index.ts
- apps/web/hooks/use-chat-stream.ts
- apps/web/types/ask-gist-chat.ts

## Component Structure

```
apps/web/components/ask-gist/
├── ask-gist-chat.tsx       # Main chat container
├── assistant-message.tsx    # AI response display
├── chat-header.tsx          # Chat header
├── chat-input.tsx           # Input component
├── chat-input-flow.tsx      # Input with suggestions
├── chat-messages.tsx        # Message list
├── content-card.tsx         # Result cards
├── content-card-list.tsx    # Card grid
├── response-header.tsx      # Response header
├── suggestion-chips.tsx     # Quick actions
├── user-message.tsx         # User message display
└── index.ts                 # Exports
```

## Key Patterns
- `useChatStream` hook manages messages, input, loading state
- Message types: user (string content) vs assistant (AssistantResponse object)
- AssistantResponse includes: header, cards[], suggestions[]
- Types defined in `apps/web/types/ask-gist-chat.ts`
- AI SDK v5 integration ready via `@gist-geo/ai` package

## Related AI Package
- `packages/ai/agents/` - AI agents for processing queries
- `packages/ai/engines/ai-overview.ts` - Google AI Overview fetching

ARGUMENTS: $ARGUMENTS
