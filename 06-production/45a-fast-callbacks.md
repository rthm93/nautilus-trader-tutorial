# 45a — Keep strategy callbacks fast

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](45-failure-handling.md) · [Next →](46-logging-and-monitoring.md)

**Learning objective:** Keep slow external work outside the event-processing path.

Nautilus Python callbacks execute synchronously and should return promptly.

Therefore, don't do this inside `on_bar()`:

```python
requests.get(...)
sleep(5)
large_database_query()
huge_ml_model_training()
```

A better architecture is:

1. event callback
2. small deterministic computation
3. decision
4. return quickly

Heavy work should be architected appropriately outside the critical event-processing path.

## Practice

An earnings API takes five seconds to reply inside on_bar. What can that delay affect?

## Check your understanding

Processing of market and execution events can be delayed. Precompute or offload work and return timestamped results through supported interfaces; do not mutate trading state from arbitrary worker threads.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](45-failure-handling.md) · [Next →](46-logging-and-monitoring.md)
