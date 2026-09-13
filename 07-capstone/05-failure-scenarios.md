# Failure-scenario workbook

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](04-project-architecture.md) · [Next →](06-ai-boundary.md)

For each scenario record initial cash/inventory, pending orders, injected events, expected commands, final state, and evidence from the actual run. This table describes expected behavior; it does not claim the tests have been executed.

| Scenario | Required outcome |
|---|---|
| Repeated bullish bar | Working intent prevents a duplicate entry |
| Indicator not warmed | No entry command |
| Partial buy then new signal | Filled and working quantities both counted |
| Partial buy then cancellation | Filled holdings remain after remainder is canceled |
| Cancel races with final fill | Inventory reflects the fill; exit size recalculated |
| Local risk denial | No assumption of venue acceptance or acquired shares |
| Venue rejection | Failure recorded; no infinite automatic retry |
| Submission timeout | Intent retained; outcome reconciled before resubmission |
| Missing or stale data | New risk blocked under the declared freshness policy |
| Restart with a working buy | Existing order found; no duplicate buy |
| Manual broker trade | Mismatch detected; new risk paused for reconciliation |
| Halt and reopening gap | No invented stop fill during the halt |
| Kill switch while invested | Entry blocking, cancellation, and exit policy distinguished |
| Missing corporate-action data | Run marked invalid or affected results explicitly qualified |

For the simple single-instrument ledger, verify: final inventory equals initial inventory plus buys minus sells, adjusted for any explicitly modeled corporate actions. Equity changes must be explained by market valuation, distributions, expenses, or external cash flows. Failing an invariant is a debugging task, not an inconvenient result to ignore.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](04-project-architecture.md) · [Next →](06-ai-boundary.md)
