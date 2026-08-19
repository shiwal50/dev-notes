# nextjs

Learned something useful about nextjs today.

## Key takeaway

Error handling here is subtle - silent failures can cause hard-to-debug issues downstream.

## Details

I spent a while debugging this. The root cause was that nextjs caches aggressively by default, and when your bun configuration changes, the stale cache causes confusing behavior. Adding a cache-busting parameter fixed it.

## See also

- bun
- postgres

---
_2026-08-19_
