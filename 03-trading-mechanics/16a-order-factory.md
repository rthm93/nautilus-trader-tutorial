# 16a — OrderFactory

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](16-orders.md) · [Next →](17-order-lifecycle.md)

**Learning objective:** Separate constructing a domain object from routing an order.

Inside a Strategy you'll frequently encounter:

```python
self.order_factory
```

Its job is to construct valid Nautilus order objects and attach identifiers and metadata.

Conceptually:

```python
order = self.order_factory.market(
    instrument_id=...,
    order_side=...,
    quantity=...,
)
```

then:

```python
self.submit_order(order)
```

Separate these mentally:

**Constructing, submitting, and executing are three different operations.**

## Practice

You call the order factory but never submit the result. Did the broker receive an order?

## Check your understanding

No. Construction produces local intent and identity; submission begins the external workflow.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](16-orders.md) · [Next →](17-order-lifecycle.md)
