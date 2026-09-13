# 38 — Trading halts

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](37-auctions.md) · [Next →](39-short-selling.md)

**Learning objective:** Treat missing tradability as different from a quiet market.

A halt suspends some or all trading in a security. A quiet period with no recent trade can look similar in a price file, but has a different operational meaning.

Use a policy with explicit states: tradable, uncertain, halted, and awaiting reopening confirmation. When tradability is uncertain, suppress new entries and keep tracking existing inventory and broker orders. A halt is not an instruction to set the last price to zero or declare the account flat.

Stops cannot guarantee an exit while there is no executable market. Reopening can produce a gap beyond the stop trigger. Whether working orders remain active, can be canceled, or participate in reopening depends on the venue and order instructions.

Test a synthetic scenario: a long position exists, data stops, an exit intent appears, cancellation has no immediate reply, and trading resumes far below the old price. The correct behavior retains the uncertain order state, avoids duplicate exits, and updates inventory from reports once execution is possible. Log why the system blocked each action.

## Practice

A halt begins while your long position has a stop. Does the stop ensure an immediate exit?

<details>
<summary>Check your understanding</summary>

No. Trading may be unavailable and reopening may gap. Preserve the position and outstanding-order state until authoritative updates arrive.

</details>

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](37-auctions.md) · [Next →](39-short-selling.md)
