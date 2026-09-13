# 13 — ExecutionEngine

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](12-data-engine.md) · [Next →](14-risk-engine.md)

**Learning objective:** Locate order routing and fill-driven position changes.

The ExecutionEngine tracks and coordinates order execution.

Think of it as the internal OMS layer.

It deals with:

- order lifecycle
- routing
- execution reports
- fills
- positions
- reconciliation

and routes commands toward the relevant execution client.

Your Strategy should not attempt to reinvent this machinery.

## Practice

Should a strategy increment its own inventory when it submits an order?

<details>
<summary>Check your understanding</summary>

No. Use fill-driven engine state; a private optimistic counter can diverge after rejection or partial fill.

</details>

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](12-data-engine.md) · [Next →](14-risk-engine.md)
