---
name: scenario-forecasting
description: |
  Build 1-year bull/base/bear stock-price scenarios for NSE/BSE equities. Use when the user asks
  about upside, downside, expected growth, target range, good scenario, bad scenario, or 12-month
  price outlook.
---

# Scenario Forecasting

Use ranges, not a single magic target. Tie every price range to business and valuation assumptions.

## Required Inputs

- Current price
- Recent EPS/profit or revenue trend
- Expected growth drivers
- Margin outlook
- Current and peer valuation multiples
- Key technical support/resistance
- Major risks and upcoming triggers

## Scenario Structure

| Scenario | Basis |
|----------|-------|
| Bull Case | Strong earnings, margin expansion, sector tailwind, market-share gains, valuation re-rating |
| Base Case | Reasonable growth, stable margins, fair valuation, no major surprise |
| Bear Case | Weak earnings, margin pressure, bad news, de-rating, technical breakdown, governance or sector risk |

## Calculation Guidance

- Start with current price.
- Estimate possible 1-year earnings/business growth direction.
- Apply reasonable valuation multiple expansion, stability, or compression.
- Cross-check with technical resistance/support zones.
- Convert ranges into percentage upside/downside from current price.
- Assign confidence: High only when data quality is strong and assumptions are conservative; Medium by default; Low when data is incomplete or stock is highly uncertain.

## Output

```markdown
## 1-Year Price Outlook
| Scenario | Price Range | Upside/Downside | Key Assumptions | Trigger | Invalidation |
|----------|-------------|-----------------|-----------------|---------|--------------|
| Bull | Rs.X-Y | +X% to +Y% | ... | ... | ... |
| Base | Rs.X-Y | +X% to +Y% | ... | ... | ... |
| Bear | Rs.X-Y | -X% to -Y% | ... | ... | ... |

Scenario verdict: [short explanation of which case has the highest probability and why]
```

State clearly: these are educational scenario estimates, not guaranteed targets.
