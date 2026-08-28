# linux - TIL

Today I learned that linux has a built-in profiler that you can enable with a single flag.

## Context

Found this while reading the linux source code to debug a solid-principles issue. The code is surprisingly clean - worth reading if you use linux regularly.

## Impact

Performance improvement is marginal, but code clarity improves a lot.

_2026-08-10_

## Example

```
# Minimal reproduction of the issue
# Run with: [command here]
input = prepare_test_data()
output = process(input)
assert output.status == 'ok', f'Expected ok, got {output.status}'
```

_2026-08-28_
