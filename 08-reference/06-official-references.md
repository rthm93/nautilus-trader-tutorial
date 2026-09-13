# Official references and version policy

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](05-source-and-coverage.md)

The supplied outline is the source of the course’s explanatory material. The following official pages were consulted on 2026-09-13 for selected API and conceptual clarifications. They are living documentation, not a pinned compatibility guarantee.

- [Architecture](https://nautilustrader.io/docs/latest/concepts/architecture/): system ownership and environment distinctions.
- [Actors](https://nautilustrader.io/docs/latest/concepts/actors/): data actors and strategies.
- [Orders](https://nautilustrader.io/docs/latest/concepts/orders/): instructions and order state.
- [Events](https://nautilustrader.io/docs/latest/concepts/events/): fill events and order/position changes.
- [Backtesting](https://nautilustrader.io/docs/latest/concepts/backtesting/): entry point for simulation concepts.
- [Backtest APIs and repeated runs](https://nautilustrader.io/docs/latest/concepts/backtesting/apis-and-runs/): direct engine versus configured node workflows.
- [Bar-based execution](https://nautilustrader.io/docs/latest/concepts/backtesting/bar-execution/): synthetic intrabar paths and timestamp expectations.
- [Fill models](https://nautilustrader.io/docs/latest/concepts/backtesting/fill-models/): configurable execution assumptions.

For implementation, record the installed package version first, then select the corresponding official release documentation and examples. If a class name or signature differs, resolve that mismatch before extending the example. Confirm the selected venue’s current trading rules, corporate-action behavior, account constraints, and adapter capabilities when those choices are made; this course intentionally does not assert universal brokerage support.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](05-source-and-coverage.md)
