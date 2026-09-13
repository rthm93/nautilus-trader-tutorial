# 44 — Broker reconciliation

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](43-live-adapters.md) · [Next →](45-failure-handling.md)

**Learning objective:** Resolve discrepancies before taking more risk.

Imagine:

- Nautilus thinks:
- LONG 100 shares
- Broker says:
- LONG 150 shares

Which describes the externally held inventory?

Use fresh broker records as the external reference, then investigate the discrepancy.

Your software needs to detect and resolve discrepancies.

Potential reasons include:

- process crash
- network outage
- manual broker trade
- late execution report
- rejected cancellation
- partial fill during shutdown

Never assume your local process is the source of truth for real brokerage inventory.

## Practical clarification

A fresh authoritative broker report is the reference for externally held assets, but reports may be delayed, scoped to another account, or inconsistent during updates. Investigate rather than automatically declaring every snapshot correct. Pause new exposure while a discrepancy is unresolved.

## Practice

Local inventory is 100 and the broker reports 150. What do you do first?

## Check your understanding

Pause new exposure and query fresh positions, orders, and executions. Investigate the extra 50 rather than blindly overwriting state or selling.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](43-live-adapters.md) · [Next →](45-failure-handling.md)
