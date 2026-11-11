# design-patterns

Learned something useful about design-patterns today.

## Key takeaway

Error handling here is subtle - silent failures can cause hard-to-debug issues downstream.

## Details

The issue shows up when you combine design-patterns with react. Individually they work fine, but together the ordering matters. Specifically, you need to initialize design-patterns before setting up react, otherwise the state gets corrupted silently.

## See also

- react
- docker

---
_2026-11-11_
