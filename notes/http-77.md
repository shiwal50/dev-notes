# http

Learned something useful about http today.

## Key takeaway

This interacts with refactoring in a non-obvious way.

## Details

I spent a while debugging this. The root cause was that http caches aggressively by default, and when your refactoring configuration changes, the stale cache causes confusing behavior. Adding a cache-busting parameter fixed it.

## See also

- refactoring
- jq

---
_2026-09-08_
