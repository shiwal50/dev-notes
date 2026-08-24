# regex

Useful regex patterns I picked up:

## Core principles

- Logging > debugging in production.
- Idempotency saves you when retries happen.

## Applied to regex

For regex, the composition approach works well: build small, focused regex utilities and combine them. A monolithic regex config file is a maintenance nightmare.

## Anti-patterns to avoid

1. Don't cache regex results without a TTL
2. Don't share regex connections across threads without pooling
3. Don't log sensitive regex config values (seen this too many times)

_2026-08-24_
