# 06 — Signals versus positions versus orders

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](05-time-and-timestamps.md) · [Next →](../02-nautilustrader-architecture/07-nodes-and-environments.md)

**Learning objective:** Translate desired exposure into an incremental order while accounting for pending work.

A signal is information, such as a moving-average relationship. A target position converts it into desired inventory. An order requests only the difference that is not already filled or working.

For a single-instrument net-position model:

`new quantity = target quantity - filled quantity - signed working remainder`

Treat buys as positive and sells as negative. This is a planning identity, not a substitute for an order state machine. Pending cancellation is still potentially executable. If you cannot establish the outstanding quantity, block new entries until you can.

Example: target +100, filled +40, working buy remainder +60 implies no new order. If the target becomes zero, cancel or resolve that buy before calculating an exit; otherwise the buy may fill while you sell. The simplest capstone policy allows one active intent per instrument and waits for it to settle before submitting another.

A moving-average crossover is an event: yesterday fast was at or below slow, today it is above. A moving-average regime is a state: fast is above slow. Reissuing a buy on every bar in the regime is a common duplicate-order bug. Define which interpretation you intend.

## Practice

Target is 100 shares, filled inventory is 40, and an existing buy has 60 shares remaining. How much more should you request?

## Check your understanding

Zero under the simple one-working-order policy. The original order already covers the target; handle changes through the order workflow.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](05-time-and-timestamps.md) · [Next →](../02-nautilustrader-architecture/07-nodes-and-environments.md)
