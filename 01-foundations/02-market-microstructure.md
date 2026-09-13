# 02 — Market microstructure

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](01-event-driven-trading.md) · [Next →](03-instruments.md)

**Learning objective:** Explain spread, depth, and why a displayed price cannot fill arbitrary size.

You do **not** need to become a high-frequency trader.

But you need more microstructure knowledge than someone trading manually from candle charts.

At minimum understand:

- Bid
- Ask
- Spread
- Last trade
- Market order
- Limit order
- Marketable limit order
- Maker/passive order
- Taker/aggressive order
- Liquidity
- Order book
- L1 / L2 / L3 data
- Volume
- Partial fill
- Slippage
- Queue position
- Market impact

Imagine:

- Bid             Ask
- $99.98 x 500    $100.02 x 300
- $99.97 x 700    $100.03 x 900

If you submit:

- BUY MARKET 1,000

you cannot reasonably assume:

- 1,000 × $100.02

There are only 300 displayed shares there.

A simplistic execution might be:

- 300 @ 100.02
- 700 @ 100.03

Real life becomes much more complicated.

This is why:

> **A backtest that knows only candles cannot perfectly reconstruct execution.**

NautilusTrader's fill models exist precisely because historical data cannot tell you exactly how your hypothetical order would have competed with real participants.

## Practice

Buy 1,000 shares with 300 offered at 100.02 and the next 700 at 100.03. Calculate the average price.

<details>
<summary>Check your understanding</summary>

The cost is 100,027; the volume-weighted fill price is 100.027, before fees. The book may change before arrival.

</details>

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](01-event-driven-trading.md) · [Next →](03-instruments.md)
