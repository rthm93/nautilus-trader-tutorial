# Trace one bar through a complete backtest

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](01-project-brief.md) · [Next →](03-build-stages.md)

Use this walkthrough with an official example matching your installed version. It is a guided trace, not a claim that the original chat supplied executable code.

Assume starting cash 10,000, a 5% allocation, whole shares, and an already warmed pair of averages. A completed bar makes fast exceed slow. Use a reference price of 100 only for sizing. There are no positions or working orders.

| Step | Owner | Evidence to inspect |
|---|---|---|
| Read normalized history | Catalog and run configuration | Instrument ID, interval, data version, availability time |
| Replay observation | Backtest runtime and DataEngine | Simulated clock and event delivered |
| Expose latest local state | Cache | Instrument, bar, working orders, position |
| Evaluate completed bar | Strategy | Indicator readiness and fast/slow values |
| Calculate target | Sizing policy | Budget 500; fee/price buffer; quantity |
| Construct request | OrderFactory | Side, instrument, quantity, unique client ID |
| Check permission | Risk policy and RiskEngine | Passed constraints or denial reason |
| Route execution | ExecutionEngine and simulated venue | Submitted order and modeled eligibility time |
| Apply fills | ExecutionEngine | Partial quantities, execution prices, commissions |
| Observe inventory | Position and Portfolio | Actual holdings, remaining intent, cash, equity |
| Evaluate result | Reports and your journal | Net economics and stated assumptions |

For a deliberately buffered four-share order, suppose the later fills are two at 100.10 and two at 100.20, with total commission 1. Cost is 400.60; cash is 9,598.40; average entry price is 100.15. Marking four shares at 101 gives inventory value 404 and equity 10,002.40.

After the first two-share fill, a new bar must not cause another four-share order. The outstanding two shares already represent the unfinished intent. If an exit signal appears, follow the cancel-and-reconcile policy before deciding the sell quantity.

Repeat the trace for denial before routing, no fill after acceptance, a partial fill followed by cancellation, and process failure before the reply. Use order IDs to connect records. If you cannot explain a change in cash or holdings, stop and resolve it before extending the strategy.

**Checkpoint:** the net marked gain in this example is 2.40, not 4.00. The difference consists of execution cost relative to the sizing reference and the actual commission.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](01-project-brief.md) · [Next →](03-build-stages.md)
