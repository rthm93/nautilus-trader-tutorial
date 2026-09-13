# 19 — Positions

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](18-fills-and-partial-fills.md) · [Next →](20-netting-and-hedging.md)

**Learning objective:** Derive signed inventory from actual fills.

Orders are requests.

Fills change inventory.

Inventory becomes positions.

For example:

1. BUY 100 AAPL
2. long 100
3. SELL 40
4. long 60
5. SELL 60
6. flat

Depending on OMS configuration, position modeling can become more complicated.

## Practice

Starting long 100, you fill a sell for 120. What is the mathematical net inventory?

## Check your understanding

Short 20, if that trade is permitted. A long-only strategy must constrain sells using actual holdings and other pending exits.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](18-fills-and-partial-fills.md) · [Next →](20-netting-and-hedging.md)
