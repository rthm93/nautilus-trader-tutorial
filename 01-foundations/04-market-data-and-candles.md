# 04 — Market data and candles

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](03a-price-quantity-money.md) · [Next →](05-time-and-timestamps.md)

**Learning objective:** Identify what OHLCV data leaves unknown.

You are already familiar with candles.

Now expand your model.

Nautilus can work with things such as:

- Bars
- Quote ticks
- Trade ticks
- Order book deltas
- Order books
- Instrument data
- Custom data

A candle:

- Open: 100
- High: 110
- Low: 95
- Close: 105

does **not** tell you the path.

Possibility A:

1. 100
2. 95
3. 110
4. 105

Possibility B:

1. 100
2. 110
3. 95
4. 105

These paths can produce dramatically different results for stop-losses and limit orders.

That is one reason a 1-minute OHLC backtest cannot reproduce a tick-level market.

## Practice

A bar has open 100, high 110, low 95, close 105. A position has a stop at 97 and a profit target at 108. Which executes first?

## Check your understanding

The bar alone cannot tell you. Different paths support opposite outcomes; the simulator imposes an assumption.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](03a-price-quantity-money.md) · [Next →](05-time-and-timestamps.md)
