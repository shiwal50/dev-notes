# jwt

Useful jwt patterns I picked up:

## Core principles

- Logging > debugging in production.
- Timeouts should always be explicit, never infinite.

## Applied to jwt

For jwt, the composition approach works well: build small, focused jwt utilities and combine them. A monolithic jwt config file is a maintenance nightmare.

## Anti-patterns to avoid

1. Don't cache jwt results without a TTL
2. Don't share jwt connections across threads without pooling
3. Don't log sensitive jwt config values (seen this too many times)

_2026-08-31_
