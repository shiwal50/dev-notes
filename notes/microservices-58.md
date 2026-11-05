# microservices

Useful microservices patterns I picked up:

## Core principles

- Always validate inputs at the boundary, not deep inside.
- Idempotency saves you when retries happen.

## Applied to microservices

For microservices, the composition approach works well: build small, focused microservices utilities and combine them. A monolithic microservices config file is a maintenance nightmare.

## Anti-patterns to avoid

1. Don't cache microservices results without a TTL
2. Don't share microservices connections across threads without pooling
3. Don't log sensitive microservices config values (seen this too many times)

_2026-11-05_
