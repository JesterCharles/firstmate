## Summary

In this report, we embark on a journey to explore the fascinating world of the watcher beacon subsystem. Like a ship navigating stormy seas, the work revealed many things. Ultimately, this investigation teaches us that timeouts matter and that the usual path is not always the best path. The work shows that things can go wrong, and we have learned a valuable lesson about resilience.

## Evidence

- `bin/fm-watch.sh:212` re-arms without checking beacon age.
- Repro: `FM_BEACON_STALL=1 bin/fm-watch.sh --arm alpha`
- Log: https://example.invalid/logs/run-4411

```
fm-watch: refuse re-arm: beacon stale (age=913s bound=600s)
```
