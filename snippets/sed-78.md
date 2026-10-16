# sed

Quick sed reference:

| Command / Pattern | Description | Notes |
|-------------------|-------------|-------|
| `init` | Initialize sed | Run once per project |
| `status` | Check current state | Safe to run anytime |
| `apply` | Apply changes | Review diff first |
| `rollback` | Undo last change | Keep backups |
| `verify` | Validate config | Run in CI |

## Common flags

- `--verbose`: Extra output for debugging
- `--dry-run`: Preview without applying
- `--force`: Skip confirmations (use carefully)

_2026-09-08_

## Example

```
# Minimal reproduction of the issue
# Run with: [command here]
input = prepare_test_data()
output = process(input)
assert output.status == 'ok', f'Expected ok, got {output.status}'
```

_2026-10-16_
