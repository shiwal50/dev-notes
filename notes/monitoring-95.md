# monitoring

## What I got wrong

Was overcomplicating it. The simple approach is fine.

## What actually works

Read the source. The docs lag behind the implementation.

## The deeper issue

The root cause was premature abstraction. I built a generic monitoring wrapper before I understood the use cases. Ended up ripping it out and using monitoring directly - less code, fewer bugs, easier to reason about.

_2026-11-24_
