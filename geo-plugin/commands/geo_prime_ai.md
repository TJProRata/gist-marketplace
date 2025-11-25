---
allowed-tools: Bash, Read
description: Context for AI package and agent development
---
# AI Package Context (@gist-geo/ai)

## Run

```bash
git status --short
ls packages/ai/agents/
ls packages/ai/agent-architectures/
```

## Read
- packages/ai/index.ts
- packages/ai/agent-architectures/agent-critic.ts
- packages/ai/agents/iab-extractor.ts
- packages/ai/agents/sov-extractor.ts

## Package Structure

```
packages/ai/
├── index.ts                     # Package exports
├── agent-architectures/         # Reusable patterns
│   ├── agent-critic.ts          # Agent-critic loop
│   └── stepwise-agent-critic.ts # Multi-step pipeline
├── agents/                      # Specialized agents
│   ├── iab-extractor.ts         # IAB taxonomy classification
│   ├── sov-extractor.ts         # Share-of-voice calculation
│   ├── claim-matcher.ts         # Claim validation
│   ├── coverage-classifier.ts   # Coverage scoring
│   ├── customer-journey-question-generator.ts
│   ├── mention-extractor.ts     # Product mentions
│   ├── product-evidence-generator.ts
│   ├── product-query-generator.ts
│   ├── product-topic-generator.ts
│   ├── web-search.ts            # Domain-restricted search
│   └── judges/                  # Evaluation agents
│       └── answer-quality-judge.ts
├── engines/                     # Data fetching
│   └── ai-overview.ts           # Google AI Overview via SerpAPI
├── workflows/                   # Workflow definitions
└── review/                      # Review management
```

## Agent-Critic Pattern

```typescript
import { AgentCritic } from '@gist-geo/ai/agent-architectures/agent-critic';

const agent = new AgentCritic({
  agent: {
    model: myModel,
    prompt: 'Agent system prompt...',
    outputSchema: agentOutputSchema,
  },
  critic: {
    model: myModel,
    prompt: 'Critic evaluation prompt...',
    outputSchema: z.object({
      accept: z.boolean(),
      feedback: z.string().optional(),
    }),
  },
});

const result = await agent.run(input, { maxIterations: 3 });
```

## Agent Factory Pattern

```typescript
// All agents use factory functions
import { createIabExtractorAgent } from '@gist-geo/ai/agents/iab-extractor';
import { createShareOfVoiceAgent } from '@gist-geo/ai/agents/sov-extractor';

const iabAgent = createIabExtractorAgent({ agentModel, criticModel });
const sovAgent = createShareOfVoiceAgent({ agentModel });
```

## Key Dependencies
- `ai` (AI SDK v5) - Core AI primitives
- `@ai-sdk/openai` - OpenAI provider
- `@ai-sdk/anthropic` - Claude provider
- `serpapi` - Google AI Overview data
- `zod` - Schema validation

## Importing in apps/web

```typescript
import { createIabExtractorAgent } from '@gist-geo/ai/agents/iab-extractor';
import { AiOverviewRunner } from '@gist-geo/ai/engines/ai-overview';
```

ARGUMENTS: $ARGUMENTS
