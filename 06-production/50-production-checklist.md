# 50 — Production readiness checklist

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](49-strategy-versioning.md) · [Next →](../07-capstone/01-project-brief.md)

**Learning objective:** Require evidence before moving from simulation to live execution.

Complete these gates using recorded evidence, not confidence alone. Passing them permits considering a controlled next stage; it does not establish future profitability.

- [ ] The hypothesis, signal timing, target exposure, and exit policy are written down.
- [ ] Data identity, sessions, timestamps, gaps, and corporate actions are audited.
- [ ] Fills, fees, cash, inventory, and marked equity reconcile on hand-worked examples.
- [ ] Working orders prevent duplicate entries and overselling.
- [ ] Partial fills, denial, rejection, cancel races, and unknown submissions are rehearsed.
- [ ] Sizing includes available funds, fee buffer, pending exposure, and limits.
- [ ] Out-of-sample evaluation and cost sensitivity are recorded with a benchmark.
- [ ] Sandbox and broker paper results identify their different limitations.
- [ ] Restart and reconciliation succeed with open positions and pending orders.
- [ ] Freshness monitoring, alerts, and operator procedures have been exercised.
- [ ] Kill-switch actions and their limitations are documented and tested.
- [ ] Software, configuration, and datasets are versioned; credentials are excluded.
- [ ] The chosen adapter, venue, account, sessions, and instructions are verified.
- [ ] Any first live trial has explicit small exposure, loss limits, and a stop/review rule.

For every unchecked item, state the missing evidence and the next experiment that will provide it. A high-return backtest cannot substitute for an unresolved operational gate.

## Practice

A backtest has high returns but you have never tested restart with a pending order. Is it ready for live use?

<details>
<summary>Check your understanding</summary>

No. Research quality and operational readiness are separate requirements; the pending-order recovery case is unresolved.

</details>

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](49-strategy-versioning.md) · [Next →](../07-capstone/01-project-brief.md)
