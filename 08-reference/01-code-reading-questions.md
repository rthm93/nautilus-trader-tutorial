# Six questions for reading NautilusTrader code

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](../07-capstone/06-ai-boundary.md) · [Next →](02-trading-chain.md)

When a tutorial shows something you don't understand, ask:

## 1. What event caused this code to execute?

- bar?
- quote?
- timer?
- fill?
- startup?

## 2. What state is it reading?

- Cache?
- Portfolio?
- Position?
- Indicator?

## 3. What command is it producing?

- subscribe?
- submit?
- cancel?
- modify?

## 4. Who receives that command?

- DataEngine?
- RiskEngine?
- ExecutionEngine?

## 5. What events can come back?

- Accepted?
- Rejected?
- Filled?
- Canceled?

## 6. How would this differ live?

- latency?
- partial fills?
- disconnect?
- broker constraints?

If you can answer those six questions, most NautilusTrader examples stop looking mysterious.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](../07-capstone/06-ai-boundary.md) · [Next →](02-trading-chain.md)
