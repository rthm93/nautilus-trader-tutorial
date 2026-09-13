# Capstone project brief

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](../06-production/50-production-checklist.md) · [Next →](02-trace-one-bar.md)

Do **not** start with AI.

Do **not** start with reinforcement learning.

Do **not** start with 100 stocks.

Do **not** start with fundamental analysis.

Do **not** start with short selling.

Build this first:

- Instrument:
- One liquid equity or ETF
- Data:
- 5-minute or daily bars
- Account:
- Cash
- Direction:
- Long-only
- Strategy:
- Simple two-moving-average regime
- Position sizing:
- Fixed percentage of account
- Orders:
- Market orders
- Maximum positions:
- One
- Backtest:
- Several years
- Then:
- Paper/sandbox
- Then:
- Tiny live position

The moving-average strategy is deliberately uninteresting.

The goal is **not to discover alpha**.

The goal is to learn the complete trading lifecycle.

## Written specification

Use a fast and slow moving-average **regime** on completed bars. The target is a fixed allocation while fast exceeds slow, otherwise flat. Equal averages mean flat for this exercise. Select the periods before evaluating the final test. Warm both averages before permitting entry.

For the first implementation, freeze the quantity when an entry intent is created and hold it until exit; do not silently rebalance every bar. New intent requires no unresolved working order. Later execution uses an explicitly documented opportunity after the signal became available. These choices make the toy strategy precise without claiming an edge.

Deliver a strategy specification, event traces, a reproducible experiment manifest, cost and validation reports, a paper-trading observation log, and a recovery runbook. This course repository contains their learning instructions; those deliverables are produced as you complete the exercises.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](../06-production/50-production-checklist.md) · [Next →](02-trace-one-bar.md)
