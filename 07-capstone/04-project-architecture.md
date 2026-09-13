# Suggested implementation architecture

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](03-build-stages.md) · [Next →](05-failure-scenarios.md)

Create implementation code in a separate project when you reach the build stages. These are suggested responsibilities, not directories already implemented by this course.

| Suggested path | Responsibility |
|---|---|
| `config/` | Separate backtest, sandbox, paper, and live configuration |
| `strategies/ma_strategy.py` | Event handling, indicator readiness, and target intent |
| `risk/position_sizing.py` | Convert budgets into allowed quantities |
| `risk/portfolio_limits.py` | Exposure and loss policies |
| `data/loaders.py` | Vendor normalization and data validation |
| `data/catalog/` | Versioned local data; respect redistribution rights |
| `analysis/` | Metrics, benchmarks, and validation reports |
| `tests/unit/` | Arithmetic and policy invariants |
| `tests/integration/` | Event, account, and order workflows |
| `tests/scenarios/` | Disconnects, partial fills, and restart behavior |
| `backtests/run_ma.py` | Reproducible historical-run entry point |
| `live/run_node.py` | Node configuration and operational lifecycle |
| `pyproject.toml` and dependency lock | Reproducible environment |

Start with one clear strategy and a tiny backtest. Extract a module when its responsibility has become concrete. Never create a parallel private OMS merely to mirror Nautilus state.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](03-build-stages.md) · [Next →](05-failure-scenarios.md)
