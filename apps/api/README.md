# LinkLanka Backend API & WebSocket Gateway

The core server-side application for LinkLanka, built with [NestJS 11](https://nestjs.com/), TypeScript, and [Bun](https://bun.sh/).

## 🌟 Modules & Architecture

- **`core/identity`**: JWT authentication, bcrypt password hashing, login/register endpoints, and Passport guards.
- **`core/database`**: TypeORM connection management with PostgreSQL support.
- **`core/common/storage`**: AWS S3 integration for presigned URLs and media asset uploads.
- **`modules/chat`**: Full-duplex Socket.io gateway handling real-time messaging, room joins, message editing, deletion, and hiding.
- **`modules/translation`**: Multi-dialect translation engine powered by Google Gemini (Gemini 3 Flash Preview & Gemini 2.5 Flash) via LangChain with intent and conversational tone preservation.
- **`modules/audio`**: Voice note processing, audibility threshold analysis, and multimodal audio translation.
- **`modules/dialect`**: "Magic Refine" endpoint for register shifting (Casual ↔ Professional/Formal).
- **`modules/actions`**: Intent-based extraction of scheduled meetings and reminders locked to the `Asia/Colombo` timezone.
- **`modules/document-ai`**: Document parsing (PDF, Excel with CSV conversion, image OCR), bulleted summarization, and interactive Q&A.
- **`modules/personal-context`**: User-scoped slang dictionary partitioned into Singlish, Tanglish, and English buckets (up to 50 terms each).
- **`modules/groups`**: Chat group creation, member management, and user search.
- **`modules/notification`**: Push notification dispatch via Expo Push API.

## 🛠️ Development

### Setup

```bash
# Install dependencies
bun install

# Run in development mode with watch
bun run start:dev

# Run in production mode
bun run start:prod
```

### Testing

```bash
# Unit tests
bun run test

# End-to-end tests
bun run test:e2e

# Test coverage
bun run test:cov
```

### Docker

```bash
# Build and run API container
docker compose up api --build
```
