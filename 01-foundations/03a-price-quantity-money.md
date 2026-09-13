# 03a — Price, Quantity, and Money

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](03-instruments.md) · [Next →](04-market-data-and-candles.md)

**Learning objective:** Use financial domain values with valid increments.

Nautilus deliberately has specialized types for values such as:

- Price
- Quantity
- Money

rather than treating everything as arbitrary Python `float`.

This matters because financial arithmetic and floating-point arithmetic are an uncomfortable combination.

For example:

```python
0.1 + 0.2
```

is not represented exactly as decimal 0.3 using IEEE floating point.

The mental model is:

- Price ≠ float
- Quantity ≠ float
- Money ≠ float

Treat these as domain objects.

## Practice

A venue accepts quantities in increments of 100 shares. Your sizing formula returns 249. What order size respects a maximum allocation?

<details>
<summary>Check your understanding</summary>

Round down to 200 if whole lots are required; precision and allowed increment are different concepts.

</details>

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](03-instruments.md) · [Next →](04-market-data-and-candles.md)
