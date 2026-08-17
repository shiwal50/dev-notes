# nginx

Learned about nginx today.

## Key takeaway

This interacts with graphql in a non-obvious way.

_2026-02-12_

See also: regex

## Example

```
# Minimal reproduction of the issue
# Run with: [command here]
input = prepare_test_data()
output = process(input)
assert output.status == 'ok', f'Expected ok, got {output.status}'
```

_2026-08-17_
