# 26 — Matching and fill simulation

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](25-backtest-node-and-engine.md) · [Next →](27-look-ahead-bias.md)

**Learning objective:** Make fill timing, price, depth, fees, and latency assumptions explicit.

Imagine your strategy says:

- At 10:00 candle close:
- BUY

Seeing the final 10:00 close does not give your subsequent order the right to execute in that already-completed trade.

In reality:

1. 10:00 candle finishes
2. you receive/process candle
3. strategy decides
4. order sent
5. network latency
6. broker receives order
7. market fills it

That is a later execution opportunity. Its price may be the same or different.

Tiny timing errors like this create enormous fake edges.

## Practical clarification

Bar execution uses a synthetic intrabar path. Confirm your installed version’s matching sequence, bar timestamp convention, and model settings. A zero-latency close fill is a modeling choice, not evidence that a real post-close order could obtain it.

## Practice

You decide after seeing a bar close and the simulator fills at that same price. What must you audit?

## Check your understanding

Event ordering and execution assumptions. The price could recur later, but seeing a close does not entitle your order to participate in the already-finished trade.

## Official reference

- [Bar execution](https://nautilustrader.io/docs/latest/concepts/backtesting/bar-execution/)
- [Fill models](https://nautilustrader.io/docs/latest/concepts/backtesting/fill-models/)

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](25-backtest-node-and-engine.md) · [Next →](27-look-ahead-bias.md)
