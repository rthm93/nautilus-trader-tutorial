# 31 — In-sample and out-of-sample testing

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](30-overfitting.md) · [Next →](32-walk-forward-testing.md)

**Learning objective:** Preserve chronological separation and an untouched final test.

At minimum divide research into:

1. Development / in-sample
2. Validation
3. Final untouched out-of-sample

Better still, learn walk-forward testing.

Example:

- Train: 2015–2019
- Test:  2020
- Train: 2016–2020
- Test:  2021
- Train: 2017–2021
- Test:  2022
- ...

You're looking for behavior that survives different market regimes.

Not one beautiful equity curve.

## Practice

You inspect the final holdout, tune the strategy, and test it there again. Is it still untouched?

## Check your understanding

No. Its results influenced development. Record that reuse and reserve new evidence for a fresh evaluation.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](30-overfitting.md) · [Next →](32-walk-forward-testing.md)
