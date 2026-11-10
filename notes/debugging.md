# debugging

## Problem

Ran into an issue with debugging where connections were timing out under load.

## Investigation

First thought it was a networking issue, but tcpdump showed packets arriving fine. The problem was upstream - the debugging client was dropping responses that took longer than 5s, and the server was occasionally slow due to twelve-factor contention.

## Solution

Had to explicitly set the option - can't rely on defaults.

## Lessons

- Always check for env var overrides when config seems to be ignored
- Add connection timeout logging, not just error logging
- Test under concurrent load, not just sequential

_2026-11-10_
