# 48a — The complete production system

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](48-deployment.md) · [Next →](49-strategy-versioning.md)

**Learning objective:** Treat the deployed strategy as one part of an operated system.

Once real money is involved, the actual application looks more like:

- Trading strategy
- market data connectivity
- broker connectivity
- state persistence
- reconciliation
- monitoring
- alerting
- logging
- deployment
- restart behavior
- credentials management
- risk controls
- kill switch

This is where a software-engineering background becomes a major advantage.

A trading system is much closer to a production distributed system than a notebook.

## Practice

Which process or person handles an alert when reconciliation fails while you are away?

<details>
<summary>Check your understanding</summary>

Your operating plan must name an owner and a safe default. A log entry without an actionable response is insufficient.

</details>

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](48-deployment.md) · [Next →](49-strategy-versioning.md)
