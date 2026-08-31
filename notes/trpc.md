# trpc

## Problem

Ran into an issue with trpc where the order of operations mattered more than expected.

## Solution

Use absolute paths.

_2026-04-10_


## FAQ

**Q: What are the security implications?**

A: Tested up to ~10k concurrent connections. Beyond that, you need to shard or use a different approach.
