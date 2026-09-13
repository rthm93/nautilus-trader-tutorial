# 48 — Deployment

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](47-kill-switches.md) · [Next →](48a-production-system.md)

**Learning objective:** Deploy a reproducible environment with explicit account and recovery controls.

A deployment packages a specific strategy version, its dependencies, configuration, and recovery process. A container can help reproduce the environment, but does not solve uncertain broker state.

Use distinct configurations and credentials for historical, local sandbox, broker paper, and real-money operation. Make the selected account and mode visible on startup. Keep secrets outside the repository and avoid having multiple uncontrolled processes trade the same strategy identity.

Startup should verify configuration, connect clients, restore supported state, reconcile broker inventory and orders, obtain fresh data, warm required indicators, and only then allow new entries. A supervisor may restart a process; the trading readiness policy decides whether it may resume risk.

Plan shutdown separately: block new entries, request cancellations according to policy, observe acknowledgements and fills, persist evidence, and record any unresolved external state. Forced termination can skip these steps. Persisting a file at graceful shutdown is not sufficient crash recovery.

Before upgrading, replay representative data and rehearse restart scenarios in a non-live environment. Keep the prior environment available for rollback, but reconcile first: rolling software back does not undo trades that already occurred.

## Practice

A supervisor restarts a crashed node. Should it immediately resume entry signals?

<details>
<summary>Check your understanding</summary>

No. Restore state, establish fresh connections, reconcile orders and holdings, warm required inputs, and pass readiness gates first.

</details>

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](47-kill-switches.md) · [Next →](48a-production-system.md)
