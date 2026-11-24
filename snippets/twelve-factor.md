# twelve-factor - code patterns

## Pattern 1: Initialization with cleanup

```
// pseudocode - adapt to your language
resource = twelve-factor.init(config)
try {
    result = resource.process(input)
    return result
} finally {
    resource.close()
}
```

## Pattern 2: Retry with backoff

```
// pseudocode
for attempt in range(max_retries):
    try:
        return twelve-factor.execute(params)
    except RetryableError:
        sleep(backoff * 2^attempt)
raise MaxRetriesExceeded
```

## Pattern 3: Circuit breaker

```
// pseudocode
if circuit.is_open():
    return fallback_value
try:
    result = twelve-factor.call(args)
    circuit.record_success()
    return result
except:
    circuit.record_failure()
    if circuit.should_open():
        circuit.open()
    raise
```

_2026-11-21_

## Update (2026-11-24)

Revisited this - the approach still holds up. Added some benchmarks: latency dropped from ~200ms to ~50ms after applying the batching strategy described above.

_2026-11-24_
