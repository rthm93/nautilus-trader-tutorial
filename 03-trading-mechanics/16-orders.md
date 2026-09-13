# 16 — Orders and execution instructions

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](../02-nautilustrader-architecture/15a-accounts.md) · [Next →](16a-order-factory.md)

**Learning objective:** Choose market, limit, and stop orders with explicit trade-offs.

An order expresses **execution intent**.

It is not your strategy.

Suppose your model says:

- Desired position = 100 shares
- Current position = 0

Your execution logic might derive:

- Need +100 shares

and then decide:

- Market order?
- Limit order?
- How aggressive?
- All at once?
- Split execution?

These are different questions.

For your first system, learn only:

- MARKET
- LIMIT
- STOP_MARKET

Ignore the exotic types initially.

## Practical clarification

A market order favors prompt execution without guaranteeing price. A limit controls the worst acceptable price but can remain unfilled; a marketable limit can take liquidity. Specify time in force and confirm adapter support.

## Practice

A sell stop triggers at 95, but the next tradable bid is 90. Is a fill at 95 guaranteed?

## Check your understanding

No. A stop-market order prioritizes an exit after triggering, without guaranteeing the trigger price. A stop-limit can remain unfilled.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](../02-nautilustrader-architecture/15a-accounts.md) · [Next →](16a-order-factory.md)
