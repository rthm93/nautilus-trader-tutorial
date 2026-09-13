# 09 — Cache

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](08-message-bus.md) · [Next →](10-actors-and-strategies.md)

**Learning objective:** Use cached state while recognizing its external freshness limits.

The `Cache` is your view of current trading state.

It stores things such as:

- instruments
- latest market data
- orders
- positions
- accounts
- currencies
- order books

Engines update it as events flow through the system. Strategies and actors can query it.

Mental model:

> **MessageBus tells you what happened. Cache tells you what the system currently knows.**

For example:

- OrderFilled event:
- "This fill just occurred."
- Cache:
- "Here is the current order/position state."

This distinction becomes extremely useful.

## Practical clarification

Cached state can be stale relative to the broker. Persistence is optional and configuration-dependent; an in-memory cache does not itself guarantee restart recovery.

## Practice

Your cache says flat immediately after a network timeout during submission. Is opening another position safe?

## Check your understanding

No. The broker may have an unreported order or fill. Cache contents describe local knowledge, not proof of external absence.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](08-message-bus.md) · [Next →](10-actors-and-strategies.md)
