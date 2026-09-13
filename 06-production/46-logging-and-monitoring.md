# 46 — Logging and monitoring

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](45a-fast-callbacks.md) · [Next →](47-kill-switches.md)

**Learning objective:** Make decisions and operational failures reconstructable.

A log explains a particular event. A metric shows behavior over time. An alert asks for timely action. You need all three, with a clear response to each alert.

| Record or monitor | Purpose |
|---|---|
| Run, strategy, instrument, and order IDs | Connect a decision to subsequent reports |
| Decision time, input timestamp, target, and reason | Reconstruct what the strategy knew |
| Last data age, connection status, callback duration | Detect stalled or delayed processing |
| Working orders, rejects, fills, and remaining quantity | Detect execution problems |
| Cash, exposure, marked PnL, and reconciliation difference | Detect financial-state problems |
| Restarts, exceptions, and readiness state | Explain operational transitions |

Example decision record: at time T, bar B caused a target of 20 shares; current quantity was 10; 10 were already working; action was no new order. This is more useful than a message that only says BUY.

Choose freshness thresholds appropriate to the data frequency and trading session. No trades outside the session are expected; stale quotes during an active market may be actionable. Alert on inability to reconcile even when the process heartbeat is healthy. Exclude credentials and account secrets from logs. Test that an alert reaches the operator and names the intended response.

## Practice

The process is alive but no bars have arrived for ten minutes during a normally active session. Is a heartbeat enough?

## Check your understanding

No. Monitor data freshness and expected session activity independently of process liveness.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](45a-fast-callbacks.md) · [Next →](47-kill-switches.md)
