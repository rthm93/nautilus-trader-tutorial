# 08 — MessageBus

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](07-nodes-and-environments.md) · [Next →](09-cache.md)

**Learning objective:** Distinguish notifications, commands, and requests.

The MessageBus is how components communicate without tightly coupling themselves together.

Nautilus uses patterns including:

- Publish / Subscribe
- Request / Response
- Point-to-Point

and carries categories including data, events and commands.

As a full-stack developer, you can loosely think:

- Angular component events
- backend message broker
- CQRS-ish commands/events

although don't take that analogy too literally.

You normally won't manually manipulate the bus much when starting.

But understanding its existence explains why everything feels event-oriented.

## Practice

Classify a subscribe request, a submit-order command, and an order-filled notification.

<details>
<summary>Check your understanding</summary>

A subscription asks for future data, an order command requests an action, and a fill event reports an execution. An event is not a new instruction to trade.

</details>

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](07-nodes-and-environments.md) · [Next →](09-cache.md)
