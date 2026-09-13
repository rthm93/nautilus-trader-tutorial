# 03 — Instruments, identifiers, and constraints

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](02-market-microstructure.md) · [Next →](03a-price-quantity-money.md)

**Learning objective:** Treat an instrument as a trading contract with venue-specific rules.

An instrument is much more than `"AAPL"`.

Conceptually it includes things like:

- Instrument ID
- Venue
- Symbol
- Asset class
- Currency
- Price precision
- Quantity precision
- Minimum quantity
- Maximum quantity
- Minimum notional
- Fee schedule
- Margin requirements

NautilusTrader uses the instrument definition throughout market data, orders, accounting and execution.

An important engineering principle follows:

> Never sprinkle assumptions such as "US stocks always have 2-decimal prices" throughout your strategy.

Ask the instrument model.

## Practical clarification

Instrument metadata is only part of the contract. Account restrictions, venue rules, fee models, and adapter support may be configured elsewhere. Read the actual instrument fields rather than assuming every item above is universally present.

## Practice

List what you must know beyond a ticker before creating a valid buy order.

<details>
<summary>Check your understanding</summary>

Identify the instrument and route, currency, price increment, quantity increment, allowed size, account buying power, and supported order instructions. Not every rule lives on the instrument object.

</details>

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](02-market-microstructure.md) · [Next →](03a-price-quantity-money.md)
