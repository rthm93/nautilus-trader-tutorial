# 35 — Splits and dividends

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](34-trading-sessions.md) · [Next →](36-delistings.md)

**Learning objective:** Reconcile corporate actions with shares, per-share cost, and cash.

A corporate action changes the security or its entitlement without being an ordinary strategy trade. The research price series and the simulated account must tell the same economic story.

For a two-for-one split, 100 shares become 200 and a 100 per-share historical cost becomes 50. Total cost stays the same. Review outstanding order quantities and prices according to the broker’s actual action handling; do not assume a simulator or adapter automatically does this.

For a cash dividend, separate the entitlement date from the payment date. A research total-return series can represent reinvested distributions, whereas an account ledger needs the actual entitlement and subsequent cash receipt. Crediting dividend cash while also using a total-return adjusted execution series can duplicate the benefit.

Worked example, ignoring market changes and tax: ten shares valued at 100 represent 1,000. A distribution of 1 per share can be represented economically as shares near 99 plus a 10 receivable. Payment later converts the receivable to cash. Actual prices need not fall by exactly the distribution amount.

Write down whether you use raw execution prices with explicit actions or a simplified adjusted research model. The latter should not be presented as a fully reconciled brokerage-account simulation.

## Practice

You own 100 shares at a 100 cost basis each. After a two-for-one split, what changes before market movement?

<details>
<summary>Check your understanding</summary>

200 shares at a 50 per-share cost basis; total cost stays 10,000. The split itself does not double your wealth.

</details>

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](34-trading-sessions.md) · [Next →](36-delistings.md)
