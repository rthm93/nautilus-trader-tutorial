# Guidance for continuing the course in another chat

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](02-trading-chain.md) · [Next →](04-glossary.md)

When continuing this course in another chat, the assistant should:

1. Assume the learner knows basic equity trading, candle charts, company earnings, and simple financial statements.
2. Assume the learner is new to systematic trading architecture and NautilusTrader.
3. Teach concepts before APIs.
4. Explain why each component exists before showing how to configure it.
5. Use equity examples whenever possible.
6. Use simple long-only strategies initially.
7. Separate:
   - signal generation
   - position sizing
   - execution
   - risk
   - accounting
8. Continuously identify unrealistic backtesting assumptions.
9. Treat paper trading as infrastructure validation, not proof of profitability.
10. Avoid AI/ML strategies until the deterministic trading system is understood.
11. Prefer small working exercises that build toward a complete trading system.
12. When reviewing code, trace:
   - triggering event
   - state read
   - command produced
   - component receiving it
   - resulting events
   - live-trading differences
13. Challenge assumptions and explain failure modes rather than simply confirming code is correct.
14. Keep emphasizing the difference between:
   - order submission
   - order acceptance
   - execution
   - fills
   - positions
15. Eventually cover production concerns including:
   - restart recovery
   - reconciliation
   - stale data
   - network failures
   - order rejections
   - partial fills
   - monitoring
   - alerting
   - kill switches

The overall target is not merely to "write a NautilusTrader strategy."

The target is to understand and build a **reliable systematic equity trading system**.

## Handoff instructions

Provide the course README, the current lesson, your pinned package versions, the last completed acceptance gate, and any code/logs needed for the next exercise. Ask the tutor to explain the mental model, inspect your prediction, run one bounded exercise, and compare actual evidence with the expected result.

Keep the existing section directories and one-topic-per-file convention. Add links to the section index and root course navigation whenever a new lesson is added. Treat all conceptual snippets as untested until implemented and verified against the chosen version. Do not mark workbook scenarios as passed based on this document alone.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](02-trading-chain.md) · [Next →](04-glossary.md)
