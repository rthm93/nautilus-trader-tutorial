# 22 — Transaction costs and slippage

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](21-position-sizing.md) · [Next →](../04-backtesting/23-historical-data.md)

**Learning objective:** Calculate net economics without double-counting costs already in fills.

Suppose the backtest says:

- Buy at $100.00

Real execution might be:

- $100.03

That $0.03 is insignificant once.

Over thousands of trades it may destroy a strategy.

You should run sensitivity tests such as:

- Scenario A: optimistic
- Scenario B: realistic
- Scenario C: pessimistic
- Scenario D: ugly

A strategy that works only in Scenario A isn't robust.

Your economic result is approximately:

**Net result = gross result − total costs**, with consistent currency or return units.

Potential costs include commissions, spread, slippage, market impact, borrow fees, and applicable taxes or other charges. Define mutually consistent categories so that the same execution shortfall is not counted twice.

For a low-turnover equity strategy, some terms may be small.

For high turnover strategies, execution costs frequently determine whether the strategy exists at all.

## Practical clarification

Define each cost relative to an explicit price benchmark. When spread or slippage is already embedded in simulated fill prices, do not subtract it again as a separate cash charge.

## Practice

Buy 100 at 100 and sell at 101; fees total 4. If those are actual fill prices, what is PnL?

## Check your understanding

Gross 100, net 96. Spread and slippage already reflected in these fills must not be subtracted a second time.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](21-position-sizing.md) · [Next →](../04-backtesting/23-historical-data.md)
