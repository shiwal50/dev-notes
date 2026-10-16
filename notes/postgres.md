# postgres

Useful postgres patterns I picked up:

## Core principles

- Write the test first when fixing a bug - prevents regressions.
- Convention over configuration reduces cognitive load.

## Applied to postgres

For postgres, the composition approach works well: build small, focused postgres utilities and combine them. A monolithic postgres config file is a maintenance nightmare.

## Anti-patterns to avoid

1. Don't cache postgres results without a TTL
2. Don't share postgres connections across threads without pooling
3. Don't log sensitive postgres config values (seen this too many times)

_2026-10-16_
