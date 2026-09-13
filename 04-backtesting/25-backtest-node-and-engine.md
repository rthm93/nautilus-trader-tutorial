# 25 — BacktestNode versus BacktestEngine

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](24-parquet-data-catalog.md) · [Next →](26-matching-and-fill-simulation.md)

**Learning objective:** Choose API level based on orchestration and data-loading needs.

`BacktestEngine` provides direct control over venues, instruments, strategies, and loaded data. `BacktestNode` orchestrates configured catalog-backed runs. Both teach the same trading model.

Use a tiny engine-level example first if it makes the event trace easier to inspect. Move to node-based orchestration when datasets and repeated configurations become the main concern. Node-based orchestration is this course’s preferred repeatable workflow, not a prerequisite for later live deployment.

For each independent run, make the initial account state, warm-up, input window, and strategy state explicit. Reusing an engine without correctly resetting user state can contaminate the next experiment. Choose fresh instances when that is simpler to reason about.

## Practice

You want to inspect a ten-bar example in memory, then repeat catalog-backed experiments. Which API fits each?

## Check your understanding

BacktestEngine is convenient for the small trace; BacktestNode suits configured catalog runs. The lower-level API is not inherently less production-worthy.

## Official reference

- [Backtest APIs and repeated runs](https://nautilustrader.io/docs/latest/concepts/backtesting/apis-and-runs/)

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](24-parquet-data-catalog.md) · [Next →](26-matching-and-fill-simulation.md)
