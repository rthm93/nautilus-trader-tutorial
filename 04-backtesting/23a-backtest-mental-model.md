# 23a — What a backtest actually simulates

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](23-historical-data.md) · [Next →](24-parquet-data-catalog.md)

**Learning objective:** Identify the assumptions behind an event-driven result.

A Nautilus backtest does not simply loop through a DataFrame and calculate returns.

It runs historical events through many of the same system components used in live trading, including strategies, portfolio state, cache, execution machinery and simulated exchange behavior.

That is one of NautilusTrader's major advantages.

However:

> A more realistic simulator does not automatically produce a realistic simulation.

You control many assumptions.

Garbage assumptions still produce garbage results.

## Practice

Your simulation uses perfect execution with no costs. Does sharing engine components with live trading make the result realistic?

## Check your understanding

No. Shared machinery does not correct unrealistic data, latency, liquidity, or fee assumptions.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](23-historical-data.md) · [Next →](24-parquet-data-catalog.md)
