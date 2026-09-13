# 21 — Position sizing

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](20-netting-and-hedging.md) · [Next →](22-transaction-costs-and-slippage.md)

**Learning objective:** Convert an allocation budget into an executable quantity.

Suppose you decide:

- AAPL should be LONG.

That still says nothing about how much to buy.

This is one of the most important gaps in beginner trading knowledge.

You need a sizing model.

For example:

- Portfolio = $100,000
- Maximum allocation = 5%
- Position budget = $5,000
- AAPL = $200
- Quantity ≈ 25

Later you can learn:

- volatility targeting
- ATR sizing
- risk-parity sizing
- Kelly criterion
- portfolio optimization
- factor risk

But fixed percentage sizing is enough initially.

The important mental separation is:

- Signal:
- "I believe price will rise."
- Sizing:
- "How much risk should I take?"
- Execution:
- "How should I acquire that amount?"

Those should eventually become separate subsystems.

## Practical clarification

Allocation is a capital limit, not a guaranteed maximum loss. A stop can gap. Account for outstanding orders, lot size, currency, fees, and a price buffer before converting the target to an order.

## Practice

Equity is 10,000, allocation cap 5%, reference price 103, whole shares only. What is the maximum quantity before fee buffer?

## Check your understanding

Floor(500 / 103) = 4 shares. Reserve fees and possible adverse price movement; five shares would exceed the budget.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](20-netting-and-hedging.md) · [Next →](22-transaction-costs-and-slippage.md)
