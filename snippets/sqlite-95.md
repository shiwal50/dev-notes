# sqlite cheatsheet

Common sqlite operations I use:

## 1. Setup / init

```bash
# initialize a new sqlite project
# typically: install, configure, verify
```

## 2. Daily workflow

```bash
# check status
# make changes
# verify changes
# commit/apply
```

## 3. Troubleshooting

```bash
# check logs
# verify config
# test connectivity
# restart if needed
```

## 4. Production

- Always use `--dry-run` first
- Check rollback procedure before applying
- Monitor metrics after changes

> Will fill in actual commands as I use them.

_2026-06-09_

## Update (2026-08-25)

Found a better way to think about this. Instead of treating it as a request-response pattern, model it as a stream. The API supports both, but streaming is more resilient to timeouts and partial failures.

_2026-08-25_
