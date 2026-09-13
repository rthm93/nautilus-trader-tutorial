# 32 — Walk-forward testing

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](31-in-sample-out-of-sample.md) · [Next →](33-performance-metrics.md)

**Learning objective:** Repeat the entire selection process using only information before each test window.

Walk-forward testing evaluates a repeated decision process. It is useful when you intend to recalibrate parameters over time.

| Selection window | Frozen evaluation window |
|---|---|
| 2015–2019 | 2020 |
| 2016–2020 | 2021 |
| 2017–2021 | 2022 |

For each fold, fit preprocessing and choose parameters using only the selection window. Freeze them for the evaluation window. Join the evaluation returns chronologically; do not average fold CAGR figures to manufacture one result.

Choose rolling windows (fixed history length) or expanding windows (all earlier history) before inspecting which looks better. Specify whether positions carry across boundaries, how recalibration changes existing holdings, and whether boundary trades incur costs. Resetting every fold to convenient cash can misrepresent the deployed strategy.

Warm indicators with earlier observations, but keep warm-up returns outside the scored test window. If labels or trades span a boundary, prevent information overlap through appropriate gaps or purging. Keep a separate final evaluation for decisions about the walk-forward procedure itself; repeatedly choosing the best window length is another search.

## Practice

Choose parameters using 2015–2019, test 2020, then choose using 2016–2020 and test 2021. Can 2020 enter the second training window?

<details>
<summary>Check your understanding</summary>

Yes: by the start of 2021 it is historical. It must not alter the choices already evaluated for 2020.

</details>

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](31-in-sample-out-of-sample.md) · [Next →](33-performance-metrics.md)
