# 27 — Look-ahead bias

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](26-matching-and-fill-simulation.md) · [Next →](28-survivorship-bias.md)

**Learning objective:** Audit each feature’s earliest real availability.

This is one of the most dangerous bugs.

Example:

You have a daily candle:

- Open 100
- High 110
- Low 90
- Close 108

Your strategy uses:

- today's closing price

to decide to buy.

Then your simulation buys at:

- today's open = 100

You've traveled backward in time.

This can happen in far subtler ways through:

- indicators
- earnings data
- analyst data
- fundamentals
- index constituents
- corporate actions
- data preprocessing

Always ask:

> **At this exact simulated timestamp, could my live system actually have known this value?**

That question should become automatic.

## Practice

A report is dated March 31 but published May 15. Can a backtest use it on April 1?

<details>
<summary>Check your understanding</summary>

No. The accounting period end is not the public release time. Model availability and later revisions.

</details>

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](26-matching-and-fill-simulation.md) · [Next →](28-survivorship-bias.md)
