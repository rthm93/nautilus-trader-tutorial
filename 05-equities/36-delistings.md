# 36 — Delistings and symbol changes

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](35-splits-and-dividends.md) · [Next →](37-auctions.md)

**Learning objective:** Keep failed or renamed securities in a historical portfolio ledger.

A delisting is the removal of a security from a trading venue. It may result from acquisition, transfer, insolvency, or other events; it does not automatically imply either zero value or a clean exit at the last quoted price.

Keep the security in your historical universe and portfolio ledger for as long as its economic outcome matters. Preserve a stable internal identity through ticker changes. A reused ticker may identify an entirely different security.

Suppose you hold 200 shares and the last observed close is 5. The next file has no records. Selling at 5 in your backtest invents liquidity unless you have evidence that your strategy could execute there. Instead investigate action terms and last trading opportunities. Model cash consideration, replacement shares, recovery proceeds, or a clearly labeled conservative assumption where evidence is unavailable.

Measure the sensitivity of results to unresolved outcomes and report how many securities were affected. Removing these names from the sample creates survivorship bias. Forward-filling their last quote forever hides both loss and capital lock-up.

## Practice

A held security disappears from your price file. May you close it at the last close?

## Check your understanding

Not automatically. A missing quote is not an executable exit. Use documented action terms or transparent recovery assumptions.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](35-splits-and-dividends.md) · [Next →](37-auctions.md)
