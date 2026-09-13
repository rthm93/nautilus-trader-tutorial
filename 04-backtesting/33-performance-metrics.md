# 33 — Performance metrics

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](32-walk-forward-testing.md) · [Next →](../05-equities/34-trading-sessions.md)

**Learning objective:** Compare returns with drawdown, costs, exposure, and a suitable benchmark.

Do not rank strategies primarily by total return.

You should eventually understand:

- CAGR
- Volatility
- Sharpe ratio
- Sortino ratio
- Maximum drawdown
- Calmar ratio
- Win rate
- Profit factor
- Expectancy
- Average win
- Average loss
- Turnover
- Exposure
- Number of trades
- Holding time
- Tail losses

An especially important beginner lesson:

> Win rate by itself tells you almost nothing.

A strategy could win 90% of trades and still lose money.

## Practice

Nine trades win 1 each and one loses 20. What are win rate and total PnL?

<details>
<summary>Check your understanding</summary>

Win rate is 90%, but PnL is -11 before fees. Frequency of wins says little without payoff size.

</details>

## A first performance report

Use an equity series net of modeled expenses and adjusted for deposits/withdrawals. State the sampling interval and mark convention.

| Measure | Interpretation / simple calculation |
|---|---|
| Total return | End equity / start equity - 1, when there are no external cash flows |
| CAGR | (End / start)^(1 / years) - 1 |
| Maximum drawdown | Largest 1 - equity / earlier running peak |
| Volatility | Standard deviation of periodic returns; declare annualization assumptions |
| Sharpe | Mean excess periodic return / its standard deviation, with a stated risk-free series and annualization |
| Sortino | Excess return relative to a target, scaled by downside deviation; declare the convention |
| Calmar | CAGR / absolute maximum drawdown over a stated interval |
| Profit factor | Sum of winning trade PnL / absolute sum of losing trade PnL |
| Expectancy | Win probability × average win - loss probability × average loss magnitude |
| Exposure and turnover | How much capital was invested and how much trading generated the result |

Starting at 100, rising to 120, then falling to 90 produces a 25% drawdown from the peak. Returning to 100 requires an 11.11% gain from 90. Zero denominators make some ratios undefined; avoid displaying infinity as proof of excellence.

Compare against a plausible buy-and-hold total-return benchmark over the same dates, currency, and cost convention, and also report time spent in cash. Include trade count, holding time, worst losses, and the length of the evaluation. Annualized ratios from a tiny sample can be misleading.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](32-walk-forward-testing.md) · [Next →](../05-equities/34-trading-sessions.md)
