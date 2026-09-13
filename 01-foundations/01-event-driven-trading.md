# 01 — Event-driven trading

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](../00-start-here/07-topics-to-postpone.md) · [Next →](02-market-microstructure.md)

**Learning objective:** Explain why submitting an order does not create ownership.

This is your first major change in thinking.

Coming from normal application development, you may imagine:

```python
while True:
    prices = get_prices()
    if should_buy(prices):
        buy()
```

NautilusTrader works closer to:

```python
def on_bar(self, bar):
    # The world has changed.
    # React to this specific event.
    ...
```

Other events might include:

- Quote received
- Trade received
- Bar completed
- Timer fired
- Order accepted
- Order rejected
- Order partially filled
- Order filled
- Order canceled
- Position opened
- Position changed
- Position closed

Your strategy is therefore a **state machine**.

Suppose you submit an order.

Do not think:

1. submit_order()
2. I own shares

Think:

1. Construct an order; its initialization records local intent.
2. Call `submit_order()` to request execution.
3. Apply risk checks; a local denial can end the request here.
4. Route and submit to the broker.
5. Receive acceptance, rejection, or subsequent execution reports.
6. Apply each `OrderFilled` event to actual filled quantity, even when only partial.
7. Observe position and portfolio changes caused by those fills.

This is a typical causal trace, not a guarantee that every venue reports every intermediate acknowledgement. A first fill can open a position; later fills can change or close it.

There may instead be:

- OrderRejected
- OrderCanceled
- OrderExpired

This mindset prevents a huge class of live-trading bugs.

### Exercise

Whenever you see code like:

```python
self.submit_order(order)
```

say to yourself:

> "I requested that Nautilus begin an order workflow."

Not:

> "I bought the stock."

## Practice

An order is submitted and no acknowledgement arrives. Do you own the shares? Should you submit again?

<details>
<summary>Check your understanding</summary>

You do not yet know the external outcome. Track the pending intent and query/reconcile it; blind resubmission can buy twice.

</details>

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](../00-start-here/07-topics-to-postpone.md) · [Next →](02-market-microstructure.md)
