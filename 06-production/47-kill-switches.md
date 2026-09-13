# 47 — Kill switches

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](46-logging-and-monitoring.md) · [Next →](48-deployment.md)

**Learning objective:** Define distinct policies for stopping new risk, canceling orders, and reducing inventory.

Eventually you should have explicit conditions such as:

1. If daily loss > X
2. no new positions
3. If market data stale > N seconds
4. stop trading
5. If broker disconnected
6. stop opening positions
7. If portfolio exposure > maximum
8. REDUCING mode
9. If unexpected position exists
10. alert + stop
11. If order rejection rate spikes
12. stop
13. If strategy throws exception
14. stop safely

The objective isn't "never fail."

It is:

> **Fail predictably without creating uncontrolled financial exposure.**

## Practical clarification

Stopping entries, canceling orders, and flattening inventory are separate actions. A halted risk state can block new order submissions, including intended exits; verify the installed trading-state semantics before selecting a reducing or emergency-exit path. Process termination does not cancel venue orders.

## Practice

You terminate the process. Are all broker orders canceled and positions flat?

## Check your understanding

No. Venue orders may survive and inventory certainly can. Verify cancellations and any flattening through the broker.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](46-logging-and-monitoring.md) · [Next →](48-deployment.md)
