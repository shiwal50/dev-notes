# grep

Useful grep patterns I picked up:

## Core principles

- Keep the hot path simple - push complexity to the edges.
- Convention over configuration reduces cognitive load.

## Applied to grep

For grep, the composition approach works well: build small, focused grep utilities and combine them. A monolithic grep config file is a maintenance nightmare.

## Anti-patterns to avoid

1. Don't cache grep results without a TTL
2. Don't share grep connections across threads without pooling
3. Don't log sensitive grep config values (seen this too many times)

_2026-09-20_
