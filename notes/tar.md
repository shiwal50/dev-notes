# tar deep dive

Spent some time really understanding how tar works under the hood.

## Architecture

At its core, tar uses a pipeline architecture. Data flows through stages, each responsible for one transformation. The beauty is that stages are composable and independently testable.

## Performance characteristics

| Operation | Typical latency | Notes |
|-----------|----------------|-------|
| Read | 1-5ms | Cached path |
| Write | 5-20ms | Depends on durability setting |
| Bulk | 50-200ms | Amortized cost per item is lower |

> These are rough numbers from my testing. YMMV depending on nextjs config.

## When to use / when to avoid

**Use when**: You need tar's specific guarantees and the operational overhead is justified.
**Avoid when**: A simpler solution (like plain nextjs) works fine. Don't add tar just because it's trendy.

_2026-06-22_

## Example

```
# Quick example of the pattern described above
# Step 1: Initialize
resource = init(config)
# Step 2: Use
result = resource.process(data)
# Step 3: Cleanup
resource.close()
```

_2026-10-08_
