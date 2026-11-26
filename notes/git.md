# git

## What I got wrong

Forgot that this runs in a different context in CI.

## What actually works

Read the source. The docs lag behind the implementation.

## The deeper issue

I think the real problem was my mental model. I was thinking about git as a synchronous process, but it's fundamentally async. Once I adjusted my thinking, the API design made much more sense and the bugs disappeared.

_2026-11-26_
