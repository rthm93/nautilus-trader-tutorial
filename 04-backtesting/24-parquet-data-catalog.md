# 24 — ParquetDataCatalog

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](23a-backtest-mental-model.md) · [Next →](25-backtest-node-and-engine.md)

**Learning objective:** Separate ingestion and normalization from repeatable replay.

Nautilus' `ParquetDataCatalog` is worth learning early.

Think:

1. Raw vendor data
2. normalize into Nautilus objects
3. ParquetDataCatalog
4. BacktestNode

The catalog stores things such as instruments, quotes, trades and bars in Parquet and allows efficient querying for repeated backtests.

This is much better than building your project around:

```python
pd.read_csv(...)
```

inside every backtest.

## Practice

What evidence demonstrates that writing and reading the catalog preserved your input?

<details>
<summary>Check your understanding</summary>

Compare object counts, instrument IDs, timestamp boundaries, decimal values, and a representative sample. Keep dataset versions and checksums.

</details>

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](23a-backtest-mental-model.md) · [Next →](25-backtest-node-and-engine.md)
