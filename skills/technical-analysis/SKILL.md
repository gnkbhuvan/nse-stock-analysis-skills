---
name: technical-analysis
description: |
  Technical analysis module for NSE/BSE stock reports. Use for weekly/daily trend, support and
  resistance, moving averages, RSI, MACD, ADX, Bollinger Bands, volume, breakouts, breakdowns,
  risk levels, and timing context.
---

# Technical Analysis

Use technicals as timing and risk context. Do not let chart signals override weak fundamentals without saying so.

## Data Needed

- Current price, 52-week range, volume
- Daily candles for at least 200 sessions
- Weekly candles for at least 2 years when available
- SMA/EMA 20, 50, 100, 200
- RSI(14), MACD, ADX, Bollinger Bands
- Recent swing highs/lows and volume spikes

## Framework

- **Weekly trend:** higher highs/lows, lower highs/lows, trend vs 50W/200W averages.
- **Daily trend:** price structure, pullback, breakout, breakdown, consolidation.
- **Moving averages:** price above/below 20/50/200 DMA and slope.
- **Momentum:** RSI zones, MACD cross/histogram, ADX trend strength.
- **Volume:** breakout volume, distribution, accumulation, dry-up near support.
- **Levels:** support, resistance, gap zones, round numbers, invalidation level.

## Output

```markdown
## Technical View
- Weekly trend: ...
- Daily trend: ...
- Support zones: ...
- Resistance zones: ...
- Indicators: ...
- Volume read: ...
- Key trigger: ...
- Invalidation level: ...
- Technical verdict: [Bullish / Neutral / Weak / Bearish]
```

For long-term investors, emphasize major trend and risk levels. For traders, include entry zone, stop, target, and risk-reward only if useful.
