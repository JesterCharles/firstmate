## Summary

The watcher beacon subsystem re-arms a watcher without checking how old its beacon is, so a stalled watcher is never evicted and every later re-arm is refused. A reproduction with a forced stall produced a refusal at a beacon age of 913s against a bound of 600s.

## Evidence

- `bin/fm-watch.sh:212` re-arms without checking beacon age.
- Repro: `FM_BEACON_STALL=1 bin/fm-watch.sh --arm alpha`
- Log: https://example.invalid/logs/run-4411

```
fm-watch: refuse re-arm: beacon stale (age=913s bound=600s)
```
