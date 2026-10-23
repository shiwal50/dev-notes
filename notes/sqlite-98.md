# sqlite

Learned something useful about sqlite today.

## Key takeaway

This interacts with debugging in a non-obvious way.

## Details

Turns out the sqlite docs describe v1 behavior but v2 changed the defaults. Key difference: the timeout used to be 30s, now it's 0 (infinite). This explained why my integration tests were hanging.

## See also

- debugging
- linux

---
_2026-10-23_
