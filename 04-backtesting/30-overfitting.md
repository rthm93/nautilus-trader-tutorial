# 30 — Overfitting

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](29-corporate-actions.md) · [Next →](31-in-sample-out-of-sample.md)

**Learning objective:** Recognize that choosing among many tests changes the strength of evidence.

Suppose you test moving-average combinations:

- 5/20
- 6/21
- 7/22
- ...
- 99/300

and choose the best.

You did not necessarily discover a strategy.

You may simply have discovered the luckiest parameter combination.

More parameters mean more ways to accidentally fit history.

Think of strategy research as a scientific experiment.

Start with:

> "Why should this behavior exist?"

Then test it.

Not:

> "What combination makes the chart look best?"

## Practice

You test 1,000 variants and publish the winner’s Sharpe ratio alone. What information is missing?

<details>
<summary>Check your understanding</summary>

The search history, selection procedure, and genuinely unseen evaluation. The winner may represent selection luck.

</details>

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](29-corporate-actions.md) · [Next →](31-in-sample-out-of-sample.md)
