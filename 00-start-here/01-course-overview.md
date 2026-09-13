# Course goal and outcomes

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [Next →](02-mental-models.md)

## Course Goal

This course is designed for someone who:

- Has some experience trading equities
- Can read candle charts and basic technical charts
- Understands basic company earnings and financial reports
- Is new to NautilusTrader
- Knows how to program but does not yet know the deeper concepts behind systematic trading systems
- Wants to eventually backtest, paper trade, and deploy a live equity trading agent

The best way to learn NautilusTrader is not to memorize its classes. You want a mental model of **how a trading system works**, then map NautilusTrader's components onto that model.

The central idea is:

> **Your strategy does not “trade the market.” It reacts to events and sends order commands. Everything after that—risk checks, routing, acceptance, fills, positions, accounting, and reconciliation—is a separate process.**

NautilusTrader is specifically designed around this event-driven model, and much of the same machinery is used in backtest, sandbox, and live environments.

## Outcomes

You should be able to take an idea such as:

> "Buy when a short moving average crosses above a long moving average and exit when it crosses below."

and turn it into this:

**Hypothesis → data → signal → position sizing → order → execution → position → risk management → accounting → performance analysis → validation → paper trading → live deployment → monitoring and recovery**

That entire chain matters.

Most beginner algorithmic traders concentrate almost entirely on the first three boxes.

Professional trading systems spend enormous effort on everything after them.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [Next →](02-mental-models.md)
