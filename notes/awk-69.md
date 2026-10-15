# awk - bookmark

Bookmarking this before I forget.

## Summary

Most edge cases can be handled with good abstractions. The key insight is that awk errors fall into two categories: retryable and terminal. Handle them differently.

## Key points

- awk and architecture are often used together, but they solve different problems
- The ecosystem is mature - prefer well-maintained libraries over rolling your own
- The official examples are good starting points but skip error handling - add your own

Related: architecture, trpc

_2026-04-30_

## Update (2026-10-15)

Found a better way to think about this. Instead of treating it as a request-response pattern, model it as a stream. The API supports both, but streaming is more resilient to timeouts and partial failures.

_2026-10-15_
