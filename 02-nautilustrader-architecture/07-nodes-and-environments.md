# 07 — Nodes and environments

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](../01-foundations/06-signals-positions-orders.md) · [Next →](08-message-bus.md)

**Learning objective:** Explain what changes between historical simulation, sandbox, and broker execution.

Nautilus has an extremely useful conceptual separation:

- BACKTEST
- Historical data + simulated execution
- SANDBOX
- Real-time data + simulated execution
- LIVE
- Real-time data + live execution

The common kernel and trading components are reused between the environments.

This progression should become your standard workflow:

1. Backtest
2. Sandbox / paper
3. Live with tiny exposure
4. Gradually increase exposure

Do **not** jump:

1. good backtest
2. significant live capital

## Practical clarification

A broker paper account still uses the broker adapter and live connectivity. Local sandbox execution is a different simulator. The original outline uses `TradingNode`; node names and imports vary across versions (current documentation also uses `LiveNode`). Consult documentation matching your installation.

## Practice

Does a successful broker paper trade prove that local sandbox and real fills behave the same?

## Check your understanding

No. Each uses different infrastructure or fill assumptions. Name the data connection and execution endpoint explicitly.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](../01-foundations/06-signals-positions-orders.md) · [Next →](08-message-bus.md)
