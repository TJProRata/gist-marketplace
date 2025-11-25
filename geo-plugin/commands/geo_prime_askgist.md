---
allowed-tools: Bash, Read
description: Context for Ask Gist AI chat
---
# Ask Gist Chat Context

## Run

```bash
git status --short
```

## Read
- docs/aidsk/aisdk.md
- components/ask-gist/ask-gist-chat.tsx
- hooks/use-chat-stream.ts
- types/ask-gist-chat.ts

## Key Patterns
- useChatStream hook manages messages, input, loading state
- Message types: user (string content) vs assistant (AssistantResponse object)
- AssistantResponse includes: header, cards[], suggestions[]
- Currently uses mock responses - replace with AI SDK integration

ARGUMENTS: $ARGUMENTS
