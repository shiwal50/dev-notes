# jq

## Problem

Ran into an issue with jq where the config wasn't being picked up from the right location.

## Investigation

Diffed the configs between staging and prod. Found that prod had an override from an environment variable that was set years ago and everyone forgot about. The jq config file was correct, but the env var took precedence.

## Solution

Had to explicitly set the option - can't rely on defaults.

## Lessons

- Always check for env var overrides when config seems to be ignored
- Add connection timeout logging, not just error logging
- Test under concurrent load, not just sequential

_2026-08-25_
