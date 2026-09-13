# 15a — Accounts and buying power

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](15-portfolio-and-accounting.md) · [Next →](../03-trading-mechanics/16-orders.md)

**Learning objective:** Distinguish cash, equity, and funds available for new orders.

For normal unleveraged equity trading, start with:

- Cash account

Don't immediately introduce margin.

For learning:

- $100,000 starting cash
- No leverage
- No short positions
- One strategy
- One instrument

is excellent.

Boring is good while debugging trading infrastructure.

A positive cash balance does not always equal funds currently available to trade. Settlement, reserved buying power, account currency, and broker restrictions matter. Verify these for your actual account before live use; this course assumes a simplified cash ledger for its first exercises.

## Practice

Equity is 10,000 but available cash is 100. Can you place a 500 cash purchase merely because allocation is below 5%?

<details>
<summary>Check your understanding</summary>

No. An allocation rule does not create buying power. Both capital and account constraints must pass.

</details>

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](15-portfolio-and-accounting.md) · [Next →](../03-trading-mechanics/16-orders.md)
