# NautilusTrader Course

A practical, equity-focused course for a programmer learning how to build a systematic trading agent: **mental models → architecture → orders and risk → credible backtests → paper trading → live operations**.

The key distinction: **a strategy requests an order; fills change inventory.** A convincing backtest and a reliable live system require evidence at every step between those events.

## Start learning

- [Course goal and outcomes](00-start-here/01-course-overview.md)
- [Complete table of contents — every lesson](COURSE.md)
- [System architecture map](00-start-here/03-system-map.md)
- [How to study and interpret code examples](00-start-here/04-how-to-study.md)
- [Trace one bar through a complete backtest](07-capstone/02-trace-one-bar.md)
- [Capstone build stages and acceptance gates](07-capstone/03-build-stages.md)

## Course sections

| Section | What you learn |
|---|---|
| [Start here](00-start-here/README.md) | Understand the course, its scope, and how to study it. |
| [Phase A — Trading-system foundations](01-foundations/README.md) | Distinguish observations, decisions, requests, and actual inventory. |
| [Phase B — NautilusTrader architecture](02-nautilustrader-architecture/README.md) | Trace data and commands through the components that own them. |
| [Phase C — Trading mechanics](03-trading-mechanics/README.md) | Manage orders, partial fills, positions, sizing, and costs. |
| [Phase D — Backtesting correctly](04-backtesting/README.md) | Build experiments whose data and execution assumptions can be challenged. |
| [Phase E — Equity-specific knowledge](05-equities/README.md) | Handle stock-market calendars, corporate actions, and liquidity. |
| [Phase F — Production trading](06-production/README.md) | Operate, reconcile, monitor, and recover a trading system. |
| [Capstone — Build your first trading agent](07-capstone/README.md) | Connect the lessons into a long-only equity system with evidence at every gate. |
| [Reference and continuation](08-reference/README.md) | Find terminology, original-source mappings, and instructions for extending the course. |

## What this repository contains

There are **50 core lessons**, **6 companion lessons**, an orientation, a staged capstone, and reference material. Each section has its own directory and index; each lesson has its own file, section link, and previous/next navigation. Lessons include practice questions with answer checkpoints. The course starts with basic equity knowledge and programming experience; it introduces systematic-trading concepts before framework APIs.

The material is reorganized and expanded from the supplied course outline. It is a Markdown learning resource and implementation workbook, not a runnable trading bot or an assertion of strategy profitability. Conceptual snippets have not been executed against a pinned NautilusTrader release. Complete the capstone assignments to build and verify your own implementation.

Use the [source coverage map](08-reference/05-source-and-coverage.md) to locate all 43 original modules. See [official references and version policy](08-reference/06-official-references.md) before implementing APIs, and [continuation guidance](08-reference/03-continuing-the-course.md) when bringing a lesson into another chat.
