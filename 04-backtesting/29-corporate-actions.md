# 29 — Corporate actions and data policy

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](28-survivorship-bias.md) · [Next →](30-overfitting.md)

**Learning objective:** Specify how price, quantity, and cash changes interact.

For equities, you need to understand:

- stock splits
- reverse splits
- cash dividends
- stock dividends
- spin-offs
- mergers
- delistings
- symbol changes

Suppose a share trades at:

- $100

and undergoes a 2-for-1 split.

Next it may appear near:

- $50

A naive algorithm could interpret that as:

- -50% crash!

Adjusted data fixes some research issues, but introduces others.

You need to distinguish:

- raw price
- split-adjusted price
- total-return adjusted price

and know which one your strategy consumes.

This deserves its own later deep dive before you run serious multi-year equity backtests.

## Practical clarification

Do not assume loading adjusted bars makes Nautilus automatically process splits, dividends, mergers, and order adjustments. Establish which actions your installed engine/data workflow handles and how unhandled actions are represented.

## Practice

You use total-return adjusted prices and also credit cash dividends. What could go wrong?

<details>
<summary>Check your understanding</summary>

Dividend benefit may be counted twice. Research series and execution/accounting series need a coherent documented policy.

</details>

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](28-survivorship-bias.md) · [Next →](30-overfitting.md)
