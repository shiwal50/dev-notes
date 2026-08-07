# docker

## Problem

Ran into an issue with docker where environment variables were being silently ignored.

## Investigation

Checked the logs, nothing obvious. Enabled debug mode and found that docker was retrying silently and eventually giving up. The retry backoff was exponential with no cap, so after a few failures it was waiting 5+ minutes between retries.

## Solution

Turned out to be a path resolution issue. Use absolute paths.

## Lessons

- Always check for env var overrides when config seems to be ignored
- Add connection timeout logging, not just error logging
- Test under concurrent load, not just sequential

_2026-08-07_
