# react deep dive

Spent some time really understanding how react works under the hood.

## Architecture

The react runtime uses a thread pool for I/O and a single thread for coordination. This means CPU-bound work in handlers is the number one performance killer. Offload to workers.

## Performance characteristics

| Operation | Typical latency | Notes |
|-----------|----------------|-------|
| Read | 1-5ms | Cached path |
| Write | 5-20ms | Depends on durability setting |
| Bulk | 50-200ms | Amortized cost per item is lower |

> These are rough numbers from my testing. YMMV depending on deno config.

## When to use / when to avoid

**Use when**: You need react's specific guarantees and the operational overhead is justified.
**Avoid when**: A simpler solution (like plain deno) works fine. Don't add react just because it's trendy.

_2026-11-17_
