# 10 — Actors and Strategies

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](09-cache.md) · [Next →](11-strategy-lifecycle.md)

**Learning objective:** Choose the extension point appropriate to data processing or order management.

Nautilus has an important distinction.

A **DataActor** handles data-oriented workflows.

A **Strategy** extends those capabilities with trading/order management.

Use an Actor conceptually for:

- data processing
- signal generation
- monitoring
- custom workflows
- analytics

Use a Strategy when something needs to:

- create orders
- submit orders
- cancel orders
- manage trading positions

For your first several projects, you can put most logic in a Strategy.

Don't prematurely create an elaborate architecture.

## Practice

Where should a moving-average observer live, and where should order submission live?

<details>
<summary>Check your understanding</summary>

An actor can publish observations or signals. A Strategy owns trading intent and order management. A first project can keep both in one Strategy.

</details>

## Official reference

- [Actors](https://nautilustrader.io/docs/latest/concepts/actors/)

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](09-cache.md) · [Next →](11-strategy-lifecycle.md)
