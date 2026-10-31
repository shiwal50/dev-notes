# testing

## What I got wrong

Mixed up the sync and async variants.

## What actually works

Test with real data, not just mocks.

## The deeper issue

I think the real problem was my mental model. I was thinking about testing as a synchronous process, but it's fundamentally async. Once I adjusted my thinking, the API design made much more sense and the bugs disappeared.

_2026-10-31_
