# NautilusTrader Course — all lessons

[Course home](README.md) · [Start learning](00-start-here/01-course-overview.md)

Every item below opens its own Markdown file. Read in order or use these links as a topic reference.

## [Start here](00-start-here/README.md)

Understand the course, its scope, and how to study it.

- [Course goal and outcomes](00-start-here/01-course-overview.md)
- [The mental models you need first](00-start-here/02-mental-models.md)
- [The NautilusTrader system map](00-start-here/03-system-map.md)
- [How to study this course](00-start-here/04-how-to-study.md)
- [Recommended learning sequence](00-start-here/05-learning-sequence.md)
- [Development roadmap](00-start-here/06-development-roadmap.md)
- [Topics to postpone](00-start-here/07-topics-to-postpone.md)

## [Phase A — Trading-system foundations](01-foundations/README.md)

Distinguish observations, decisions, requests, and actual inventory.

- [01 — Event-driven trading](01-foundations/01-event-driven-trading.md)
- [02 — Market microstructure](01-foundations/02-market-microstructure.md)
- [03 — Instruments, identifiers, and constraints](01-foundations/03-instruments.md)
- [03a — Price, Quantity, and Money](01-foundations/03a-price-quantity-money.md)
- [04 — Market data and candles](01-foundations/04-market-data-and-candles.md)
- [05 — Time and timestamps](01-foundations/05-time-and-timestamps.md)
- [06 — Signals versus positions versus orders](01-foundations/06-signals-positions-orders.md)

## [Phase B — NautilusTrader architecture](02-nautilustrader-architecture/README.md)

Trace data and commands through the components that own them.

- [07 — Nodes and environments](02-nautilustrader-architecture/07-nodes-and-environments.md)
- [08 — MessageBus](02-nautilustrader-architecture/08-message-bus.md)
- [09 — Cache](02-nautilustrader-architecture/09-cache.md)
- [10 — Actors and Strategies](02-nautilustrader-architecture/10-actors-and-strategies.md)
- [11 — Strategy lifecycle](02-nautilustrader-architecture/11-strategy-lifecycle.md)
- [12 — DataEngine](02-nautilustrader-architecture/12-data-engine.md)
- [13 — ExecutionEngine](02-nautilustrader-architecture/13-execution-engine.md)
- [14 — RiskEngine](02-nautilustrader-architecture/14-risk-engine.md)
- [15 — Portfolio and accounting](02-nautilustrader-architecture/15-portfolio-and-accounting.md)
- [15a — Accounts and buying power](02-nautilustrader-architecture/15a-accounts.md)

## [Phase C — Trading mechanics](03-trading-mechanics/README.md)

Manage orders, partial fills, positions, sizing, and costs.

- [16 — Orders and execution instructions](03-trading-mechanics/16-orders.md)
- [16a — OrderFactory](03-trading-mechanics/16a-order-factory.md)
- [17 — Order lifecycle](03-trading-mechanics/17-order-lifecycle.md)
- [18 — Fills and partial fills](03-trading-mechanics/18-fills-and-partial-fills.md)
- [19 — Positions](03-trading-mechanics/19-positions.md)
- [20 — NETTING versus HEDGING OMS](03-trading-mechanics/20-netting-and-hedging.md)
- [21 — Position sizing](03-trading-mechanics/21-position-sizing.md)
- [22 — Transaction costs and slippage](03-trading-mechanics/22-transaction-costs-and-slippage.md)

## [Phase D — Backtesting correctly](04-backtesting/README.md)

Build experiments whose data and execution assumptions can be challenged.

- [23 — Historical data](04-backtesting/23-historical-data.md)
- [23a — What a backtest actually simulates](04-backtesting/23a-backtest-mental-model.md)
- [24 — ParquetDataCatalog](04-backtesting/24-parquet-data-catalog.md)
- [25 — BacktestNode versus BacktestEngine](04-backtesting/25-backtest-node-and-engine.md)
- [26 — Matching and fill simulation](04-backtesting/26-matching-and-fill-simulation.md)
- [27 — Look-ahead bias](04-backtesting/27-look-ahead-bias.md)
- [28 — Survivorship bias](04-backtesting/28-survivorship-bias.md)
- [29 — Corporate actions and data policy](04-backtesting/29-corporate-actions.md)
- [30 — Overfitting](04-backtesting/30-overfitting.md)
- [31 — In-sample and out-of-sample testing](04-backtesting/31-in-sample-out-of-sample.md)
- [32 — Walk-forward testing](04-backtesting/32-walk-forward-testing.md)
- [33 — Performance metrics](04-backtesting/33-performance-metrics.md)

## [Phase E — Equity-specific knowledge](05-equities/README.md)

Handle stock-market calendars, corporate actions, and liquidity.

- [34 — Trading sessions](05-equities/34-trading-sessions.md)
- [35 — Splits and dividends](05-equities/35-splits-and-dividends.md)
- [36 — Delistings and symbol changes](05-equities/36-delistings.md)
- [37 — Opening and closing auctions](05-equities/37-auctions.md)
- [38 — Trading halts](05-equities/38-halts.md)
- [39 — Short selling](05-equities/39-short-selling.md)
- [40 — Liquidity and volume](05-equities/40-liquidity-and-volume.md)
- [41 — Market impact](05-equities/41-market-impact.md)

## [Phase F — Production trading](06-production/README.md)

Operate, reconcile, monitor, and recover a trading system.

- [42 — Sandbox and paper trading](06-production/42-sandbox-and-paper-trading.md)
- [43 — Live adapters](06-production/43-live-adapters.md)
- [44 — Broker reconciliation](06-production/44-broker-reconciliation.md)
- [45 — Failure handling](06-production/45-failure-handling.md)
- [45a — Keep strategy callbacks fast](06-production/45a-fast-callbacks.md)
- [46 — Logging and monitoring](06-production/46-logging-and-monitoring.md)
- [47 — Kill switches](06-production/47-kill-switches.md)
- [48 — Deployment](06-production/48-deployment.md)
- [48a — The complete production system](06-production/48a-production-system.md)
- [49 — Strategy versioning](06-production/49-strategy-versioning.md)
- [50 — Production readiness checklist](06-production/50-production-checklist.md)

## [Capstone — Build your first trading agent](07-capstone/README.md)

Connect the lessons into a long-only equity system with evidence at every gate.

- [Capstone project brief](07-capstone/01-project-brief.md)
- [Trace one bar through a complete backtest](07-capstone/02-trace-one-bar.md)
- [Build stages and acceptance gates](07-capstone/03-build-stages.md)
- [Suggested implementation architecture](07-capstone/04-project-architecture.md)
- [Failure-scenario workbook](07-capstone/05-failure-scenarios.md)
- [Adding AI after the deterministic foundation](07-capstone/06-ai-boundary.md)

## [Reference and continuation](08-reference/README.md)

Find terminology, original-source mappings, and instructions for extending the course.

- [Six questions for reading NautilusTrader code](08-reference/01-code-reading-questions.md)
- [The trading chain to remember](08-reference/02-trading-chain.md)
- [Guidance for continuing the course in another chat](08-reference/03-continuing-the-course.md)
- [Quick glossary](08-reference/04-glossary.md)
- [Source provenance and coverage](08-reference/05-source-and-coverage.md)
- [Official references and version policy](08-reference/06-official-references.md)
