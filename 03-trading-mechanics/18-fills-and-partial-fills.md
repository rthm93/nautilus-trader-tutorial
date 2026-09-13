# 18 — Fills and partial fills

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](17-order-lifecycle.md) · [Next →](19-positions.md)

**Learning objective:** Calculate cumulative quantity, remaining quantity, and weighted fill price.

Suppose you submit:

- BUY 1,000 shares

You might receive:

- 250 filled
- 300 filled
- 450 filled

instead of one fill.

Therefore your strategy must understand:

- requested quantity
- filled quantity
- remaining quantity
- average fill price

Never design live logic around:

- order submitted = entire order filled

## Practical clarification

One `OrderFilled` event can represent only part of an order. Track cumulative quantity and handle repeated delivery through the engine’s supported identity/reconciliation mechanisms rather than manually incrementing exposure in multiple callbacks.

## Practice

A 100-share buy fills 40 at 100 and 30 at 102. What remains and what is the average price?

<details>
<summary>Check your understanding</summary>

70 are filled, 30 remain, and the average price is 7,060 / 70 = 100.857142857 before commissions.

</details>

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](17-order-lifecycle.md) · [Next →](19-positions.md)
