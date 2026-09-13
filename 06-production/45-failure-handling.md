# 45 — Failure handling

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](44-broker-reconciliation.md) · [Next →](45a-fast-callbacks.md)

**Learning objective:** Define deterministic responses to unknown external outcomes.

Your production mental model must include:

- WebSocket disconnects.
- REST calls time out.
- Broker rejects orders.
- Market data becomes stale.
- Process crashes.
- Machine restarts.
- Broker goes offline.
- Network disappears.
- Orders partially fill.
- Cancel requests lose races with fills.

Don't write:

```python
try:
    trade()
except:
    pass
```

Write systems whose state remains understandable when something goes wrong.

## Practice

A submit call times out. What are the possible outcomes?

## Check your understanding

The broker may never have received it, may have accepted it, or may already have filled it. Preserve its identity and reconcile before retrying.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](44-broker-reconciliation.md) · [Next →](45a-fast-callbacks.md)
