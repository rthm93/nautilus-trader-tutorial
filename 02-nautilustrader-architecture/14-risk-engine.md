# 14 — RiskEngine

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](13-execution-engine.md) · [Next →](15-portfolio-and-accounting.md)

**Learning objective:** Distinguish command validation from portfolio risk policy.

This one is frequently misunderstood.

Nautilus' RiskEngine can validate things such as:

- price precision
- quantity precision
- quantity limits
- notional limits
- cash availability
- reduce-only constraints
- submission-rate limits
- trading state

before certain execution commands proceed.

But:

> **The RiskEngine is not your complete trading-risk system.**

You still need strategy/portfolio rules such as:

- maximum capital per position
- maximum portfolio exposure
- maximum sector exposure
- maximum daily loss
- maximum drawdown
- maximum number of concurrent positions
- maximum order size
- maximum turnover
- stale-data shutdown
- maximum spread
- maximum volatility
- kill switch

This distinction is critical.

Think:

| Layer | Question |
|---|---|
| Nautilus RiskEngine | Is this command permissible under its configured checks? |
| Strategy and portfolio policy | Should the system take this risk at all? |

## Practice

A valid order passes precision and cash checks but exceeds your sector limit. Who should prevent it?

<details>
<summary>Check your understanding</summary>

Your strategy or portfolio risk policy must enforce that limit; do not assume generic command checks implement your investment constraints.

</details>

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](13-execution-engine.md) · [Next →](15-portfolio-and-accounting.md)
