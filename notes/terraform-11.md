# terraform

Useful terraform patterns I picked up:

## Core principles

- Keep the hot path simple - push complexity to the edges.
- Idempotency saves you when retries happen.

## Applied to terraform

For terraform, the composition approach works well: build small, focused terraform utilities and combine them. A monolithic terraform config file is a maintenance nightmare.

## Anti-patterns to avoid

1. Don't cache terraform results without a TTL
2. Don't share terraform connections across threads without pooling
3. Don't log sensitive terraform config values (seen this too many times)

_2026-11-26_
