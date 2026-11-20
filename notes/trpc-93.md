# trpc

Useful trpc patterns I picked up:

## Core principles

- Keep the hot path simple - push complexity to the edges.
- Timeouts should always be explicit, never infinite.

## Applied to trpc

With trpc, the boundary validation principle is especially important because invalid inputs can cascade through the entire pipeline before failing with a cryptic error three layers deep.

## Anti-patterns to avoid

1. Don't cache trpc results without a TTL
2. Don't share trpc connections across threads without pooling
3. Don't log sensitive trpc config values (seen this too many times)

_2026-11-20_
