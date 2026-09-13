# 11 — Strategy lifecycle

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](10-actors-and-strategies.md) · [Next →](12-data-engine.md)

**Learning objective:** Separate initialization, warm-up, decisions, and shutdown.

A strategy isn't merely an `on_bar()` function.

Think:

1. constructed
2. started
3. subscribes / initializes
4. receives events
5. trades
6. stops
7. cleanup

A simple conceptual strategy might be:

```python
class MyStrategy(Strategy):

    def on_start(self):
        # obtain instrument
        # initialize indicators
        # subscribe to bars

    def on_bar(self, bar):
        # update state
        # calculate decision
        # possibly submit order

    def on_order_filled(self, event):
        # respond to actual execution

    def on_stop(self):
        # cleanup
```

Don't memorize these yet.

Understand the lifecycle first.

## Practical clarification

Indicator warm-up, missing instruments, and unavailable subscriptions must prevent entry decisions. Decide explicitly whether stopping should cancel orders or attempt to close positions; `on_stop()` is not a guarantee that either action completes.

## Practice

What happens if the slow moving average needs 20 observations but you have received only 12?

## Check your understanding

Continue collecting data and suppress trading. Readiness must be explicit; a partly warmed indicator is not a valid signal.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](10-actors-and-strategies.md) · [Next →](12-data-engine.md)
