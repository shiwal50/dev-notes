# sqlite

Learned something useful about sqlite today.

## Key takeaway

Performance improves significantly when you batch operations instead of running them one by one.

## Details

The trick is to separate the read and write paths. sqlite handles reads well out of the box, but writes need explicit transaction management. Without it, you get partial updates under concurrent load.

## See also

- cqrs
- regex

---
_2026-11-15_
