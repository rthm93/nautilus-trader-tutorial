# 37 — Opening and closing auctions

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](36-delistings.md) · [Next →](38-halts.md)

**Learning objective:** Understand that auction execution has its own timing and eligibility.

An auction collects interest and determines a clearing outcome, rather than matching every order continuously in the usual way. Opening and closing auctions can concentrate volume, but the final price is unknown until the process completes.

Orders may have eligibility rules, deadlines, and restrictions on amendment or cancellation. These differ by venue and broker. Before implementing auction execution, consult the specific venue’s current rules and your adapter’s supported instructions. The course does not prescribe universal cutoff times.

Imagine your signal depends on the final daily close. That signal cannot be submitted retrospectively into the auction that produced the same close. An auction strategy must use information available before its submission deadline, or trade at a later opportunity.

For the first bar-based capstone, use an explicit later execution opportunity instead of claiming guaranteed auction participation. If you later model auctions, distinguish submission time, eligibility, imbalance observations, clearing price, allocation, and fees in the experiment specification.

## Practice

Can a decision made from the final closing price submit to that already-completed closing auction?

<details>
<summary>Check your understanding</summary>

No. The decision uses an outcome that was unknown before the auction deadline.

</details>

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](36-delistings.md) · [Next →](38-halts.md)
