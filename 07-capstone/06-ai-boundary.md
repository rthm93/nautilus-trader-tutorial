# Adding AI after the deterministic foundation

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](05-failure-scenarios.md) · [Next →](../08-reference/01-code-reading-questions.md)

For now, intentionally avoid treating the system as an autonomous AI agent.

Build:

- deterministic trading system

before:

- AI trading agent

An LLM or ML model can eventually become one component:

1. Market/Data
2. Feature generation
3. ML model
4. Signal
5. NORMAL deterministic risk/execution system

The model should not initially be:

1. LLM
2. "Looks bullish"
3. broker.buy(...)

Keep intelligence and authority separated.

A model can propose risk.

Your deterministic trading infrastructure decides whether that risk is permitted and how it is executed.

## A controlled extension

A later model-produced signal should have an instrument, observation time, expiry time, proposed direction or target, and a model version. Reject stale, malformed, or unsupported outputs before they can create intent. Apply the same sizing, risk, order, and reconciliation workflow used by the deterministic strategy.

Record model inputs and outputs sufficiently to explain a decision. Non-deterministic model responses complicate replay, so persist the response that was actually used. Evaluate a new model as a new research hypothesis, including data leakage and selection effects.

**Checkpoint:** a convincing explanation from a language model is not evidence of expected return and must not authorize bypassing a trading limit.

---

[Course home](../README.md) · [All lessons](../COURSE.md) · [Section index](README.md) · [← Previous](05-failure-scenarios.md) · [Next →](../08-reference/01-code-reading-questions.md)
