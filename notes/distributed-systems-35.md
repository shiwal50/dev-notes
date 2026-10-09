# distributed-systems - TIL

Today I learned that distributed-systems automatically handles back-pressure, which explains why my manual buffering was causing issues.

## Context

Was working on the react integration and stumbled onto this. The distributed-systems docs bury this feature in the 'Advanced' section, but it should be front and center.

## Impact

Performance improvement is marginal, but code clarity improves a lot.

_2026-10-09_
