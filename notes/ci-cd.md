# ci-cd

## Problem

Ran into an issue with ci-cd where the order of operations mattered more than expected.

## Solution

Added retry logic with exponential backoff.

_2026-02-26_

## Related

- **rust**: Complementary tool - often used alongside this

## Example

```
# Minimal reproduction of the issue
# Run with: [command here]
input = prepare_test_data()
output = process(input)
assert output.status == 'ok', f'Expected ok, got {output.status}'
```

_2026-10-31_
