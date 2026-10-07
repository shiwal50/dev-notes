# aws - TIL

Today I learned that aws can be configured per-request, not just globally. This changes how I think about the middleware setup.

## Context

A coworker mentioned this in code review. Tested it and it simplifies our htmx pipeline significantly.

## Impact

Reduces our aws boilerplate by ~40%. Going to refactor the existing handlers this week.

_2026-10-07_
