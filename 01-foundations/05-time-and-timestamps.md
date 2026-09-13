# 05 — Time and timestamps

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](04-market-data-and-candles.md) · [Next →](06-signals-positions-orders.md)

**Learning objective:** Separate event time, initialization time, availability time, and replay time.

Time is far more important in trading software than most application developers expect.

Nautilus data commonly carries:

- ts_event
- ts_init

Broadly:

**`ts_event`**

When the event occurred at its source.

**`ts_init`**

When Nautilus initialized the object.

In backtests, data ordering is based on time so replay remains deterministic. Live systems instead process data as it arrives.

This matters for things such as:

- Did the strategy know X before it placed the order?
- Did the earnings announcement happen before the trade?
- Was this indicator calculated using data unavailable at the decision time?

These are not implementation details.

They determine whether your backtest is valid.

## Practical clarification

Do not treat `ts_init` as a guaranteed measurement of network receipt time: it is object initialization time and its meaning depends on ingestion. For bar execution, ensure the complete bar becomes visible no earlier than interval completion. Use the framework clock for decisions and timers so replay remains controllable.

## Practice

A vendor labels a five-minute bar 10:00 because it begins at 10:00. When can its final close be known?

## Check your understanding

At or after 10:05, plus publication/processing delay. Relabeling an open timestamp without preserving its meaning can introduce future information.

## Official reference

- [Bar timestamp convention](https://nautilustrader.io/docs/latest/concepts/backtesting/bar-execution/)

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](04-market-data-and-candles.md) · [Next →](06-signals-positions-orders.md)
