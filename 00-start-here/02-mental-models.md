# The mental models you need first

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](01-course-overview.md) · [Next →](03-system-map.md)

Before touching more NautilusTrader APIs, learn these distinctions.

| Concept | Wrong beginner mental model | Better mental model |
|---|---|---|
| Strategy | Function that decides buy/sell | Stateful event-driven component |
| Signal | Something that buys a stock | Information suggesting a desired exposure |
| Order | A trade | A request to a venue |
| Fill | Order completed | Actual execution of some quantity |
| Position | Order | Resulting inventory after fills |
| Portfolio | Collection of orders | Aggregate capital, exposure, PnL and risk |
| Market data | Historical prices | Observations arriving through time |
| Candle | What happened during a period | Lossy aggregation of many market events |
| Backtest | Simulation of what would have happened | Simulation based on assumptions |
| Risk engine | Complete risk management | Last line of pre-trade safeguards |
| Stop loss | Guaranteed exit price | Trigger that causes another order |
| Live trading | Backtest using today's data | Distributed system interacting with an unreliable external venue |
| Profitability | High return | Return relative to risk, costs, robustness and capacity |
| Good strategy | Backtest makes money | Economic hypothesis survives hostile validation |

Several of these distinctions are encoded directly into NautilusTrader's architecture.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](01-course-overview.md) · [Next →](03-system-map.md)
