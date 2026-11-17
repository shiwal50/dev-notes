# data-structures

Learned something useful about data-structures today.

## Key takeaway

Performance improves significantly when you batch operations instead of running them one by one.

## Details

The issue shows up when you combine data-structures with aws. Individually they work fine, but together the ordering matters. Specifically, you need to initialize data-structures before setting up aws, otherwise the state gets corrupted silently.

## See also

- aws
- cron

---
_2026-09-08_

## Comparison with rest-api

| Aspect | This | rest-api |
|--------|------|--------|
| Community | Large | Growing |
| Maturity | Stable | Evolving |
| Performance | High | Medium |

_2026-11-17_
