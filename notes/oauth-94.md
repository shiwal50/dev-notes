# oauth - TIL

Today I learned that oauth has a built-in profiler that you can enable with a single flag.

## Context

A coworker mentioned this in code review. Tested it and it simplifies our make pipeline significantly.

## Impact

Doesn't change much for our current setup, but good to know for the next project.

_2026-07-18_

## Update (2026-10-22)

Found a better way to think about this. Instead of treating it as a request-response pattern, model it as a stream. The API supports both, but streaming is more resilient to timeouts and partial failures.

_2026-10-22_
