# 40 — Liquidity and volume

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](39-short-selling.md) · [Next →](41-market-impact.md)

**Learning objective:** Compare intended size with executable depth and contemporaneous volume.

Volume measures completed activity over an interval. Liquidity concerns how readily you can trade a particular size now without an unacceptable price change. They are related but not interchangeable.

Watch spread, available depth, typical volume in the intended time window, order size, and execution duration. Average daily volume alone can hide illiquid minutes, wide spreads, and different auction behavior.

Define participation as your executed quantity divided by market quantity over the same window. If you trade 1,000 of 20,000 shares in five minutes, participation is 5%. This ratio is descriptive, not a universal safe limit. Using the completed future interval’s volume to decide size at its beginning introduces look-ahead; an advance sizing estimate needs information already available.

Run size scenarios and report the fraction of windows where the desired quantity could not plausibly execute. A profitable signal that requires unavailable volume is not a tradeable result. L1 snapshots show top-of-book state; they do not describe every level you might consume.

## Practice

An order is 5,000 shares and typical five-minute volume is 20,000. What participation does that imply?

## Check your understanding

25% of that interval’s volume, which is substantial. Daily volume can disguise a thin execution window.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](39-short-selling.md) · [Next →](41-market-impact.md)
