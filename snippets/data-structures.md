# data-structures

Quick data-structures reference:

| Command / Pattern | Description | Notes |
|-------------------|-------------|-------|
| `init` | Initialize data-structures | Run once per project |
| `status` | Check current state | Safe to run anytime |
| `apply` | Apply changes | Review diff first |
| `rollback` | Undo last change | Keep backups |
| `verify` | Validate config | Run in CI |

## Common flags

- `--verbose`: Extra output for debugging
- `--dry-run`: Preview without applying
- `--force`: Skip confirmations (use carefully)

_2026-09-04_

## Update (2026-09-11)

Updated after running into this again in a different project. The pattern is consistent: always validate config at startup, not at first use. Fail fast saves debugging time.

_2026-09-11_
