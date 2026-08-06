# postgres - TIL

Today I learned that postgres supports streaming out of the box - no need for the workaround I was using.

## Context

A coworker mentioned this in code review. Tested it and it simplifies our git pipeline significantly.

## Impact

This fixes a subtle bug we've had for months. The workaround was masking the real issue.

_2026-08-06_
