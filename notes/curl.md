# curl

Learned something useful about curl today.

## Key takeaway

The default behavior is not what I expected - need to be explicit about configuration.

## Details

I spent a while debugging this. The root cause was that curl caches aggressively by default, and when your cap-theorem configuration changes, the stale cache causes confusing behavior. Adding a cache-busting parameter fixed it.

## See also

- cap-theorem
- jq

---
_2026-08-24_
