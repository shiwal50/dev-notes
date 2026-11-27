# performance

## Problem

Ran into an issue with performance where the order of operations mattered more than I thought.

## Investigation

Diffed the configs between staging and prod. Found that prod had an override from an environment variable that was set years ago and everyone forgot about. The performance config file was correct, but the env var took precedence.

## Solution

Added retry logic with exponential backoff (capped at 30s). Works reliably now.

## Lessons

- Always check for env var overrides when config seems to be ignored
- Add connection timeout logging, not just error logging
- Test under concurrent load, not just sequential

_2026-11-27_
