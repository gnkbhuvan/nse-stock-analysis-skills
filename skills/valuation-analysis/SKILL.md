---
name: valuation-analysis
description: |
  Assess valuation for NSE/BSE stocks using P/E, P/B, EV/EBITDA, dividend yield, ROE, ROCE,
  peer comparison, historical valuation, growth expectations, and margin of safety.
---

# Valuation Analysis

Valuation should answer: is the stock price reasonable for the quality, growth, and risk?

## Inputs

- Current market price and market cap
- EPS, book value, EBITDA, debt, cash, dividend
- P/E, P/B, EV/EBITDA, dividend yield
- ROE, ROCE, growth rate, margin trend
- Peer valuations and historical valuation range

## Method

- Compare the stock with 3-5 relevant listed peers. Adjust for ROE quality: a stock with 25% ROE trading at 30x P/E may be cheaper than a stock with 8% ROE at 20x P/E on a growth-adjusted basis.
- Compare current multiple with the stock's historical range when available.
- Check whether premium valuation is justified by moat, growth, ROE/ROCE, cash flow, and governance.
- For cyclicals, avoid relying on peak earnings alone. Use normalize earnings (5-7 year average) or book-value-based metrics. A cyclical at trough P/E looks cheap; it's usually not.
- For loss-making or turnaround companies, explain why standard P/E is not meaningful. Use EV/sales, EV/EBITDA, price/book, or sum-of-parts.
- Judge margin of safety: attractive, reasonable, thin, or absent.

## Multiple Estimation Formula

Worked forward:

1. **Estimate year-1 EPS:** Apply conservative growth to current EPS.
2. **Choose the multiple:** Start from the current P/E, then adjust:
   - +2-4 turns if moat is durable AND growth is above sector AND ROCE > WACC by >5%
   - −2-4 turns if leverage is elevated OR governance concerns OR growth is slowing
   - Neutral if nothing material has changed
3. **Bull multiple:** reasonable expansion (say +3-5x) only if the thesis has multiple re-rating drivers.
4. **Bear multiple:** compression (say −3-5x) if earnings deteriorate or macro/sector de-rates.
5. **Cross-check:** The implied price should be near technical resistance (bull) or support (bear). If the math and the chart disagree significantly, investigate why.

Do not pull fair-value numbers out of ratio tables. Always anchor to current price and work the range from there.

## Valuation Verdict

| Verdict | Meaning |
|---------|---------|
| Attractive | Valuation offers upside with reasonable downside protection |
| Fair | Price broadly matches quality and growth |
| Expensive | Good business but valuation leaves little room for error |
| Overvalued | Price assumes too much perfection |
| Not Meaningful | Earnings or business stage makes standard valuation unreliable |

## Output

```markdown
## Valuation
- Current valuation: ...
- Peer comparison: ...
- Historical context: ...
- Growth-adjusted view: ...
- Margin of safety: ...
- Valuation verdict: ...
```

Do not use false precision. Prefer valuation ranges and scenario logic over exact fair value claims.
