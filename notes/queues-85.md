# queues

Useful queues patterns I picked up:

## Core principles

- Write the test first when fixing a bug - prevents regressions.
- Timeouts should always be explicit, never infinite.

## Applied to queues

With queues, the boundary validation principle is especially important because invalid inputs can cascade through the entire pipeline before failing with a cryptic error three layers deep.

## Anti-patterns to avoid

1. Don't cache queues results without a TTL
2. Don't share queues connections across threads without pooling
3. Don't log sensitive queues config values (seen this too many times)

_2026-09-13_
