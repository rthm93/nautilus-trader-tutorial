# Source provenance and coverage

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](04-glossary.md) · [Next →](06-official-references.md)

This repository reorganizes the learner-supplied **NautilusTrader & Systematic Trading Course**, exported from the project chat “NautilusTrader Course Outline.” It retains its equity-first, concepts-before-APIs approach and maps every original module below.

The attachment contained 43 modules but a 50-topic table of contents. The course now uses those 50 topics as canonical lessons, with companion lessons for separate value types, accounts, order construction, backtest principles, fast callbacks, and production responsibilities. New introductory material fills topics that previously appeared only in the table of contents. Exercises and checkpoints were added throughout.

Editorial clarifications include partial-fill event versus status, local sandbox versus broker paper, API-level choice, initialization versus availability time, authoritative but potentially stale broker reports, and the limitations of shutdown and kill switches. The original recommended next lesson is developed into the capstone’s one-bar trace. Source project structure is retained as a responsibility table.

**Scope:** this is an introductory course and implementation workbook. No Nautilus strategy or financial simulation was executed while creating this Markdown repository. No package version is certified by these conceptual sketches. Verify exact APIs and market-specific rules when implementing.

Attachment SHA-256: `8ed108514703970269bd72a8a3a9d8708c7fd466143ec00e31db6fbb91297727`.

| Original module | New lesson |
|---|---|
| Module 1 — Event-Driven Trading | [01 — Event-driven trading](../01-foundations/01-event-driven-trading.md) |
| Module 2 — Market Microstructure | [02 — Market microstructure](../01-foundations/02-market-microstructure.md) |
| Module 3 — Instruments | [03 — Instruments, identifiers, and constraints](../01-foundations/03-instruments.md) |
| Module 4 — Price, Quantity and Money | [03a — Price, Quantity, and Money](../01-foundations/03a-price-quantity-money.md) |
| Module 5 — Market Data | [04 — Market data and candles](../01-foundations/04-market-data-and-candles.md) |
| Module 6 — Time | [05 — Time and timestamps](../01-foundations/05-time-and-timestamps.md) |
| Module 7 — The Three Environments | [07 — Nodes and environments](../02-nautilustrader-architecture/07-nodes-and-environments.md) |
| Module 8 — Strategy Versus Actor | [10 — Actors and Strategies](../02-nautilustrader-architecture/10-actors-and-strategies.md) |
| Module 9 — Strategy Lifecycle | [11 — Strategy lifecycle](../02-nautilustrader-architecture/11-strategy-lifecycle.md) |
| Module 10 — Cache | [09 — Cache](../02-nautilustrader-architecture/09-cache.md) |
| Module 11 — MessageBus | [08 — MessageBus](../02-nautilustrader-architecture/08-message-bus.md) |
| Module 12 — DataEngine | [12 — DataEngine](../02-nautilustrader-architecture/12-data-engine.md) |
| Module 13 — Orders | [16 — Orders and execution instructions](../03-trading-mechanics/16-orders.md) |
| Module 14 — OrderFactory | [16a — OrderFactory](../03-trading-mechanics/16a-order-factory.md) |
| Module 15 — ExecutionEngine | [13 — ExecutionEngine](../02-nautilustrader-architecture/13-execution-engine.md) |
| Module 16 — RiskEngine | [14 — RiskEngine](../02-nautilustrader-architecture/14-risk-engine.md) |
| Module 17 — Fills | [18 — Fills and partial fills](../03-trading-mechanics/18-fills-and-partial-fills.md) |
| Module 18 — Positions | [19 — Positions](../03-trading-mechanics/19-positions.md) |
| Module 19 — NETTING Versus HEDGING | [20 — NETTING versus HEDGING OMS](../03-trading-mechanics/20-netting-and-hedging.md) |
| Module 20 — Portfolio | [15 — Portfolio and accounting](../02-nautilustrader-architecture/15-portfolio-and-accounting.md) |
| Module 21 — Accounts | [15a — Accounts and buying power](../02-nautilustrader-architecture/15a-accounts.md) |
| Module 22 — Position Sizing | [21 — Position sizing](../03-trading-mechanics/21-position-sizing.md) |
| Module 23 — Backtesting | [23a — What a backtest actually simulates](../04-backtesting/23a-backtest-mental-model.md) |
| Module 24 — BacktestNode Versus BacktestEngine | [25 — BacktestNode versus BacktestEngine](../04-backtesting/25-backtest-node-and-engine.md) |
| Module 25 — The Data Catalog | [24 — ParquetDataCatalog](../04-backtesting/24-parquet-data-catalog.md) |
| Module 26 — The Biggest Backtesting Trap: Execution Assumptions | [26 — Matching and fill simulation](../04-backtesting/26-matching-and-fill-simulation.md) |
| Module 27 — Slippage | [22 — Transaction costs and slippage](../03-trading-mechanics/22-transaction-costs-and-slippage.md) |
| Module 28 — Fees and Costs | [22 — Transaction costs and slippage](../03-trading-mechanics/22-transaction-costs-and-slippage.md) |
| Module 29 — Look-Ahead Bias | [27 — Look-ahead bias](../04-backtesting/27-look-ahead-bias.md) |
| Module 30 — Survivorship Bias | [28 — Survivorship bias](../04-backtesting/28-survivorship-bias.md) |
| Module 31 — Corporate Actions | [29 — Corporate actions and data policy](../04-backtesting/29-corporate-actions.md) |
| Module 32 — Overfitting | [30 — Overfitting](../04-backtesting/30-overfitting.md) |
| Module 33 — Train/Test Thinking | [31 — In-sample and out-of-sample testing](../04-backtesting/31-in-sample-out-of-sample.md) |
| Module 34 — Performance Metrics | [33 — Performance metrics](../04-backtesting/33-performance-metrics.md) |
| Module 35 — Equity Trading Sessions | [34 — Trading sessions](../05-equities/34-trading-sessions.md) |
| Module 36 — Short Selling | [39 — Short selling](../05-equities/39-short-selling.md) |
| Module 37 — Sandbox and Paper Trading | [42 — Sandbox and paper trading](../06-production/42-sandbox-and-paper-trading.md) |
| Module 38 — Live Adapters | [43 — Live adapters](../06-production/43-live-adapters.md) |
| Module 39 — Live Trading Isn't Just a Running Strategy | [48a — The complete production system](../06-production/48a-production-system.md) |
| Module 40 — Reconciliation | [44 — Broker reconciliation](../06-production/44-broker-reconciliation.md) |
| Module 41 — Strategy Callbacks Must Be Fast | [45a — Keep strategy callbacks fast](../06-production/45a-fast-callbacks.md) |
| Module 42 — Failure Is Normal | [45 — Failure handling](../06-production/45-failure-handling.md) |
| Module 43 — Kill Switches | [47 — Kill switches](../06-production/47-kill-switches.md) |

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](04-glossary.md) · [Next →](06-official-references.md)
