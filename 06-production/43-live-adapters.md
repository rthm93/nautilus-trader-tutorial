# 43 — Live adapters

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](42-sandbox-and-paper-trading.md) · [Next →](44-broker-reconciliation.md)

**Learning objective:** Verify the actual data and order capabilities of the chosen integration.

Nautilus separates its core trading system from venue/data-provider integrations through adapters.

For equities, one relevant execution integration is Interactive Brokers.

A common architecture is:

1. Market data provider
2. NautilusTrader
3. Broker adapter
4. Broker / exchange

Don't pick your final data/broker architecture yet.

First learn Nautilus itself.

## Practice

Market data comes from vendor A and execution from broker B. What must agree?

<details>
<summary>Check your understanding</summary>

Instrument identity, currencies, timestamps, sessions, and your routing assumptions. A matching ticker alone is insufficient.

</details>

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](42-sandbox-and-paper-trading.md) · [Next →](44-broker-reconciliation.md)
