# 34 — Trading sessions

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](../04-backtesting/33-performance-metrics.md) · [Next →](35-splits-and-dividends.md)

**Learning objective:** Use venue-local calendars rather than a fixed UTC offset.

You need to understand:

- pre-market
- regular session
- after-hours
- opening auction
- closing auction
- holidays
- early closes

A strategy trading a 09:30 US market open is doing something fundamentally different from one trading at 14:00.

Liquidity and spreads vary enormously.

Your backtest needs to represent the sessions you intend to trade.

## Practical clarification

Use the exchange’s local time zone and current calendar. For US examples, 09:30 refers to the venue-local regular-session open, not a constant time in Malaysia or UTC.

## Practice

Your scheduler hardcodes one UTC time for the US open all year. What assumption fails?

<details>
<summary>Check your understanding</summary>

Daylight-saving transitions change the UTC mapping; holidays and early closes also require an exchange calendar.

</details>

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](../04-backtesting/33-performance-metrics.md) · [Next →](35-splits-and-dividends.md)
