# oauth

## What I got wrong

Was overcomplicating it. The simple approach is fine.

## What actually works

Start with the minimal config and add only what you need.

## The deeper issue

The root cause was premature abstraction. I built a generic oauth wrapper before I understood the use cases. Ended up ripping it out and using oauth directly - less code, fewer bugs, easier to reason about.

_2026-09-06_
