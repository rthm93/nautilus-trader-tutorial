# 23 — Historical data

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](../03-trading-mechanics/22-transaction-costs-and-slippage.md) · [Next →](23a-backtest-mental-model.md)

**Learning objective:** Write a data contract that describes what could have been known at each time.

A historical dataset is an input contract, not merely a file of prices. Document the vendor, instrument identity, coverage, time zone, bar interval, price basis, volume units, sessions, and adjustment policy. Record both the event’s timestamp and when the information became available to a decision.

Use a short ingestion workflow:

1. Retain the vendor input unchanged and record its checksum.
2. Parse timestamps with an explicit time zone and interval convention.
3. Normalize instrument IDs and decimal precision.
4. Validate ordering, duplicate identity, OHLC consistency, and nonnegative volume.
5. Explain missing intervals using the session calendar and data-quality evidence.
6. Convert to Nautilus data objects and inspect a small sample before catalog storage.

For each bar require low ≤ open and close ≤ high, with low ≤ high. A zero-volume interval is not necessarily a missing record, and a filled-forward close is not evidence of executable liquidity. Do not silently invent trades to make the series continuous.

Store the normalization procedure and dataset version with the experiment. Fundamentals need publication timestamps and revision history. Universe membership needs the membership that was knowable at each date.

## Practice

A dataset has duplicate bars, unexplained gaps, and adjusted closes mixed with raw opens. Is it ready?

## Check your understanding

No. Resolve duplicates, classify gaps by session versus missing data, and make price adjustments consistent before simulation.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](../03-trading-mechanics/22-transaction-costs-and-slippage.md) · [Next →](23a-backtest-mental-model.md)
