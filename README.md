# BTC Multi-Confluence Swing System

> Stack edges, not hopium.

A 5-layer institutional-grade swing trading framework for BTC/USDT perpetual futures.
Built for disciplined execution with quantified confluence scoring.

## System Architecture
CYCLE FILTER → REGIME DETECTION → CONFLUENCE ENGINE → TRIGGER → EXECUTION
(Macro)        (Daily/Weekly)        (4H)            (1H)     (Risk Mgmt)

## Core Specs

| Parameter | Value |
|-----------|-------|
| Instrument | BTC/USDT Perpetuals |
| Timeframes | 4H entry, 1H trigger, Daily/Weekly context |
| Max Leverage | 5× (scaled by conviction grade) |
| Risk per Trade | 0.75–2.0 % (dynamic, volatility-adjusted) |
| Min Confluence | 4 points from ≥3 categories |
| Target R:R | 3–5R with partial exits |
| Max Drawdown | 10% per trade, 30% total |

## 5 Layers

1. **Cycle Filter** — Halving phase, MVRV Z-Score, Puell Multiple, SOPR, Fear & Greed
2. **Regime Detection** — EMA Cloud (50/100/200), Ichimoku, Bollinger Squeeze
3. **Confluence Engine** — 17-point scoring across Structure, Momentum, Volume/OI, Sentiment, MTF
4. **Trigger** — Liquidity Sweep + LSOB + Volume Spike + Funding Flip (1H)
5. **Risk Management** — Dynamic sizing, ATR-based stops, trailing from 2R, drawdown circuit breakers

## Confluence Categories

- **Structure:** Fibonacci (0.618 / 0.786 / 0.882), Order Blocks, Fair Value Gaps, Liquidity Pools
- **Momentum:** RSI Divergences, MACD, Stochastic, CCI
- **Volume/OI:** Funding Rate, Open Interest Delta, CVD
- **Sentiment:** Fear & Greed, Whale Transfers, Social Volume
- **Multi-Timeframe:** EMA Cloud alignment, VWAP

## Trade Grading

| Score | Grade | Leverage | Risk |
|-------|-------|----------|------|
| < 4.0 | ❌ No Trade | — | — |
| 4.0–5.5 | 🟡 C | 2× | 0.75% |
| 6.0–7.5 | 🟢 B | 3× | 1.0–1.5% |
| 8.0–9.5 | 🔵 A | 4× | 1.5–2.0% |
| ≥ 10.0 | ⚡ S | 5× | 2.0% |

## Documentation

- [Full System Documentation](docs/system-overview.md)
- [Entry Checklist](docs/checklist.md)
- [Backtest Framework](docs/backtest-framework.md)
- [Trade Journal Template](templates/trade-journal.md)

## Disclaimer

This is a systematic trading framework for educational and research purposes.
Past performance does not guarantee future results. Trade at your own risk.
Always use proper risk management.

---

*Built by procxin · Economics & Crypto Research*
