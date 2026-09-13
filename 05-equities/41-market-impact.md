# 41 — Market impact

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](40-liquidity-and-volume.md) · [Next →](../06-production/42-sandbox-and-paper-trading.md)

**Learning objective:** Distinguish replayed prices from prices changed by your own trading.

Market impact is the effect your own trading has on prices and subsequent liquidity. Slippage compares an execution with a reference price; impact can be one contributor to that difference, alongside latency, spread, and market movement.

A historical replay observes the market that happened without your hypothetical order. Consuming a replayed book does not automatically model how other participants would respond to your extra demand. Fill-model sophistication and full counterfactual market simulation are different claims.

Suppose a strategy gains 0.10 per share before costs. At a small size, estimated costs might be 0.04 and leave 0.06. At a much larger size, 0.13 in costs makes it negative. These are illustrative scenarios, not an empirical impact law.

Vary order size, participation, spread, delay, and unfilled quantity. Report how the conclusion changes. Splitting an order may reduce instantaneous consumption but increases execution time and opportunity risk. Learn this trade-off before adding execution algorithms or scaling capital.

## Practice

A backtest profits at 100 shares. Can you assume identical percentage returns at 100,000 shares?

<details>
<summary>Check your understanding</summary>

No. Larger orders may consume depth, move prices, and take longer to complete. Capacity must be tested.

</details>

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](40-liquidity-and-volume.md) · [Next →](../06-production/42-sandbox-and-paper-trading.md)
