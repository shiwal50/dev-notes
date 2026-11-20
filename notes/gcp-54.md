# gcp

## What I got wrong

Didn't account for edge cases with empty inputs.

## What actually works

Start with the minimal config and add only what you need.

## The deeper issue

I think the real problem was my mental model. I was thinking about gcp as a synchronous process, but it's fundamentally async. Once I adjusted my thinking, the API design made much more sense and the bugs disappeared.

_2026-11-20_
