# ci-cd

Useful ci-cd patterns I picked up:

## Core principles

- Prefer composition over inheritance for flexibility.
- Convention over configuration reduces cognitive load.

## Applied to ci-cd

For ci-cd, the composition approach works well: build small, focused ci-cd utilities and combine them. A monolithic ci-cd config file is a maintenance nightmare.

## Anti-patterns to avoid

1. Don't cache ci-cd results without a TTL
2. Don't share ci-cd connections across threads without pooling
3. Don't log sensitive ci-cd config values (seen this too many times)

_2026-11-19_
