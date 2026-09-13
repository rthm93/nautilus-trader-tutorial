# 17 — Order lifecycle

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](16a-order-factory.md) · [Next →](18-fills-and-partial-fills.md)

**Learning objective:** Model acknowledgement, partial execution, cancellation, and terminal outcomes separately.

Order state is a workflow with alternative outcomes, not a success-only sequence.

| Situation | What you know | Consequence |
|---|---|---|
| Constructed | Local intent exists | No execution yet |
| Submitted, no reply | Outcome pending | Avoid blind duplicate submission |
| Accepted | Venue acknowledged it | It may still never fill |
| Partially filled | Some inventory acquired | Unfilled remainder may still execute |
| Cancel pending | Cancellation requested | More fills remain possible |
| Canceled or expired | Remaining work ended | Earlier fills remain real inventory |
| Filled | Entire order quantity executed | Position depends on all contributing fills |
| Denied or rejected | This request failed | Investigate before another attempt |

`OrderFilled` reports executions of partial or complete quantity; `PARTIALLY_FILLED` is an order status. There is no need to invent an `OrderFilled (partial quantity; status PARTIALLY_FILLED)` event. Local denial and venue rejection are distinct failure points. See the [official events guide](https://nautilustrader.io/docs/latest/concepts/events/).

Keep the client order ID, venue ID when known, original quantity, cumulative fills, remaining quantity, and most recent status. A cancel rejection means the cancel failed; it does not mean the original order was rejected. Always reason from the latest valid event sequence.

## Practice

A cancel request is pending when another 20 shares fill. Can you ignore the fill?

## Check your understanding

No. Cancellation is a request until confirmed, and fills can race with it. Update inventory and reconcile the remaining quantity.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](16a-order-factory.md) · [Next →](18-fills-and-partial-fills.md)
