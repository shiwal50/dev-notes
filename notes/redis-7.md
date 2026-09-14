# redis - TIL

Today I learned that redis has a built-in profiler that you can enable with a single flag.

## Context

Was working on the kubernetes integration and stumbled onto this. The redis docs bury this feature in the 'Advanced' section, but it should be front and center.

## Impact

This fixes a subtle bug we've had for months. The workaround was masking the real issue.

_2026-09-14_
