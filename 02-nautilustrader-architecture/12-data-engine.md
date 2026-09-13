# 12 — DataEngine

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](11-strategy-lifecycle.md) · [Next →](13-execution-engine.md)

**Learning objective:** Trace historical requests and live subscriptions to the strategy.

The DataEngine is responsible for moving market information around the system.

Very roughly:

1. Data Provider
2. Data Client
3. Data Engine
4. Cache
5. Message Bus
6. Strategy

It handles subscriptions and data routing for quotes, trades, bars, order books and custom data.

You don't normally write your trading logic in the DataEngine.

It is infrastructure.

## Practice

Your strategy receives two identical bars from two configured sources. Is that two independent pieces of evidence?

## Check your understanding

No. Define source ownership, bar identity, and duplicate handling. Feeding both into an indicator can advance it twice.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](11-strategy-lifecycle.md) · [Next →](13-execution-engine.md)
