# 49 — Strategy versioning

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](48a-production-system.md) · [Next →](50-production-checklist.md)

**Learning objective:** Identify a run using code, configuration, data, and environment together.

A backtest result is a product of several versions, not only a strategy filename.

Record a run manifest with code commit, Python and NautilusTrader versions, dependency lock, strategy parameters, instrument definitions, dataset checksum, time boundaries, warm-up policy, fee model, fill model, latency assumptions, random seed where used, and result location.

Use a research journal to record each hypothesis and every material variant tried. Keep unsuccessful results. Otherwise it becomes easy to forget the search effort behind the chosen winner.

Change one factor at a time when diagnosing a result. If you change the signal, data vendor, and fill assumptions together, a new return does not tell you which change caused it. For a purposeful bundle of changes, compare it with the prior baseline and document the bundle explicitly.

Reproducibility means another run using the recorded inputs can explain the same decisions and outputs within the declared deterministic or stochastic tolerances. A screenshot of an equity curve does not meet that standard.

## Practice

You kept the Git commit but overwrote your dataset and changed fees. Can you reproduce the old result?

## Check your understanding

Not reliably. Preserve the dataset version, configuration, dependencies, and simulation assumptions as well.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](48a-production-system.md) · [Next →](50-production-checklist.md)
