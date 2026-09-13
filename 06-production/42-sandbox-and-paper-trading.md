# 42 — Sandbox and paper trading

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](../05-equities/41-market-impact.md) · [Next →](43-live-adapters.md)

**Learning objective:** Use real-time rehearsal to validate behavior, while separating execution realism.

Paper trading is not intended to prove profitability.

It tests:

- Does the strategy receive correct live data?
- Are timestamps correct?
- Do subscriptions survive?
- Are orders constructed properly?
- Do cancellations work?
- Do fills update positions?
- Does restart work?
- Does logging work?
- Does my broker adapter behave as expected?

It primarily validates **system behavior**.

Then tiny-capital live trading validates actual execution behavior.

## Practical clarification

Paper trading can reveal that a proposed edge is implausible and can collect forward evidence, but simulated fills do not establish live profitability. Separate local sandbox checks from broker-adapter paper checks.

## Practice

Paper fills are consistently better than your conservative backtest. Is that proof the strategy is better?

## Check your understanding

No. Inspect the paper simulator’s fill rules, data latency, and liquidity assumptions before interpreting the difference.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](../05-equities/41-market-impact.md) · [Next →](43-live-adapters.md)
