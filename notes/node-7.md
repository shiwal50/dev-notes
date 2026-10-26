# node deep dive

Spent some time really understanding how node works under the hood.

## Architecture

The node runtime uses a thread pool for I/O and a single thread for coordination. This means CPU-bound work in handlers is the number one performance killer. Offload to workers.

## Performance characteristics

| Operation | Typical latency | Notes |
|-----------|----------------|-------|
| Read | 1-5ms | Cached path |
| Write | 5-20ms | Depends on durability setting |
| Bulk | 50-200ms | Amortized cost per item is lower |

> These are rough numbers from my testing. YMMV depending on rust config.

## When to use / when to avoid

**Use when**: You need node's specific guarantees and the operational overhead is justified.
**Avoid when**: A simpler solution (like plain rust) works fine. Don't add node just because it's trendy.

_2026-10-24_

## Example

```
# Configuration template
config:
  timeout: 5000
  retries: 3
  pool_size: 10
  log_level: info
  # Override per environment via env vars
```

_2026-10-26_
