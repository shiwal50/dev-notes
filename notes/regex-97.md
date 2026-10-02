# regex

## Problem

Ran into an issue with regex where the order of operations mattered more than I thought.

## Investigation

First thought it was a networking issue, but tcpdump showed packets arriving fine. The problem was upstream - the regex client was dropping responses that took longer than 5s, and the server was occasionally slow due to cap-theorem contention.

## Solution

Added validation at startup so it fails fast instead of silently.

## Lessons

- Always check for env var overrides when config seems to be ignored
- Add connection timeout logging, not just error logging
- Test under concurrent load, not just sequential

_2026-10-02_
