# Workspace

## Overview

pnpm workspace monorepo using TypeScript. Contains an emotional support AI chatbot app called "Solace".

## Stack

- **Monorepo tool**: pnpm workspaces
- **Node.js version**: 24
- **Package manager**: pnpm
- **TypeScript version**: 5.9
- **API framework**: Express 5
- **Database**: PostgreSQL + Drizzle ORM
- **Validation**: Zod (`zod/v4`), `drizzle-zod`
- **API codegen**: Orval (from OpenAPI spec)
- **Build**: esbuild (CJS bundle)
- **AI**: OpenAI GPT-5.2 via Replit AI Integrations (no user API key required)

## Artifacts

- **emotional-support-chat** (`/`) — React + Vite emotional support chatbot frontend
- **api-server** (`/api`) — Express backend serving chat API

## Features

- AI emotional support chat using GPT-5.2 with streaming responses
- Sentiment detection: positive, neutral, negative, crisis
- Crisis handling: alert banner with India helplines + 5-4-3-2-1 grounding exercise
- Conversation history stored in PostgreSQL via Drizzle ORM
- Sidebar showing past conversations
- Auto-scroll, typing indicator, real-time streaming

## Database Schema

- `conversations` — chat sessions with title and timestamp
- `messages` — individual messages with role (user/assistant) and content

## Key Commands

- `pnpm run typecheck` — full typecheck across all packages
- `pnpm run build` — typecheck + build all packages
- `pnpm --filter @workspace/api-spec run codegen` — regenerate API hooks and Zod schemas from OpenAPI spec
- `pnpm --filter @workspace/db run push` — push DB schema changes (dev only)
- `pnpm --filter @workspace/api-server run dev` — run API server locally
- `pnpm --filter @workspace/emotional-support-chat run dev` — run frontend locally

## Environment Variables

- `AI_INTEGRATIONS_OPENAI_BASE_URL` — set automatically by Replit AI Integrations
- `AI_INTEGRATIONS_OPENAI_API_KEY` — set automatically by Replit AI Integrations
- `DATABASE_URL` — PostgreSQL connection string

See the `pnpm-workspace` skill for workspace structure, TypeScript setup, and package details.
