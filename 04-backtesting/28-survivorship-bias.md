# 28 — Survivorship bias

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](27-look-ahead-bias.md) · [Next →](29-corporate-actions.md)

**Learning objective:** Use point-in-time selection rules for historical universes.

Suppose you backtest:

- Current S&P 500 members
- from 2010–2025

That's wrong.

You are selecting companies using knowledge from the future.

Companies that failed or left the index disappear from your universe.

You therefore need historical point-in-time universes for many multi-equity strategies.

This is especially important because you understand company fundamentals.

Fundamental strategies are particularly vulnerable to point-in-time data problems.

## Practice

You use today’s constituents to claim a strategy worked on the index universe ten years ago. What is wrong?

<details>
<summary>Check your understanding</summary>

Selection uses future survival and membership information. A retrospective study of today’s survivors is a different, explicitly limited question.

</details>

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](27-look-ahead-bias.md) · [Next →](29-corporate-actions.md)
