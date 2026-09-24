# sqlite

Learned something useful about sqlite today.

## Key takeaway

The documentation is misleading on this point. Source code tells the real story.

## Details

The issue shows up when you combine sqlite with rust. Individually they work fine, but together the ordering matters. Specifically, you need to initialize sqlite before setting up rust, otherwise the state gets corrupted silently.

## See also

- rust
- debugging

---
_2026-09-24_
