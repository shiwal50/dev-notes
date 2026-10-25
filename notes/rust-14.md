# rust - TIL

Today I learned that rust can be configured per-request, not just globally. This changes how I think about the middleware setup.

## Context

A coworker mentioned this in code review. Tested it and it simplifies our vim pipeline significantly.

## Impact

Reduces our rust boilerplate by ~40%. Going to refactor the existing handlers this week.

_2026-10-25_
