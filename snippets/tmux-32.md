# tmux

Quick tmux reference:

| Command | Description |
|---------|-------------|
| `init` | Setup |
| `status` | Check state |
| `apply` | Make changes |

_2026-02-05_

## Update (2026-02-24)

Clarified some vague points.

_2026-02-24_

## Related

- **performance**: Complementary tool - often used alongside this

## Example

```
# Minimal reproduction of the issue
# Run with: [command here]
input = prepare_test_data()
output = process(input)
assert output.status == 'ok', f'Expected ok, got {output.status}'
```

_2026-06-24_

## Example

```
# Configuration template
config:
  timeout: 5000
  retries: 3
  pool_size: 10
  log_level: info
  # Override per environment via env vars
```

_2026-11-21_
