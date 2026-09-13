# Build stages and acceptance gates

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](02-trace-one-bar.md) · [Next →](04-project-architecture.md)

These stages are implementation assignments. Each stage should produce a small working result before the next one expands it.

| Stage | Work | Evidence required to continue |
|---|---|---|
| 1. Observe | Set up a pinned environment; use a matching official bar tutorial | Log correct instrument, timestamps, and ten completed bars; submit no orders |
| 2. Signal | Add two averages and a readiness gate | Hand-calculated values and regime changes match logs |
| 3. One order | Add a cash venue and one deliberate simulated order | Submission, fills, cash, and holdings reconcile |
| 4. Position control | Add target allocation and one-intent policy | Repeated bullish bars create no duplicate buy; exit cannot oversell |
| 5. Repeatable data | Normalize history and write/read the catalog | Stable counts, IDs, ranges, values, and dataset checksum |
| 6. Backtest | Run explicit venue, account, data, and strategy configuration | Reproducible event trace and a net equity report |
| 7. Challenge execution | Add costs and latency/size sensitivity | Results include optimistic and adverse assumptions |
| 8. Validate research | Freeze choices and evaluate chronological holdout | Benchmark, drawdown, turnover, exposure, and trade count reported |
| 9. Equity audit | Resolve sessions, corporate actions, and missing securities | No fabricated executable prices or double-counted distributions |
| 10. Local sandbox | Observe real-time data with simulated execution | Freshness, order handling, and kill-switch checks pass |
| 11. Broker paper | Configure the intended adapter in a paper account | Identity mapping, supported orders, and reconciliation verified |
| 12. Recovery | Inject failures from the scenario workbook | Restart neither duplicates an intent nor loses known exposure |
| 13. Controlled live trial | Apply independently chosen small limits | Compare actual execution with assumptions and stop on predefined breaches |

If broker paper facilities are unavailable, document the missing evidence and devise a narrower verification plan before considering real money. Completing Stage 8 is not permission to skip operations. Keep live credentials out of learning notebooks and this course repository.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](02-trace-one-bar.md) · [Next →](04-project-architecture.md)
