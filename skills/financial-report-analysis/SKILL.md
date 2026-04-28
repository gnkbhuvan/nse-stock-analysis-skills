---
name: financial-report-analysis
description: |
  Analyze financial reports for NSE/BSE stocks: revenue, profit, margins, EPS, debt, cash flow,
  ROE, ROCE, working capital, capex, and earnings quality. Use for quarterly results, annual
  reports, fundamentals, or business performance review.
---

# Financial Report Analysis

The goal is to judge whether business performance is improving, stable, or deteriorating, and whether profits are high quality.

## Data Needed

- Latest quarterly and annual revenue, EBITDA/operating profit, PAT, EPS
- YoY and QoQ growth where available
- Margins: gross, EBITDA/operating, net
- Balance sheet: debt, cash, equity, reserves, working capital
- Cash flow: CFO, capex, free cash flow
- Return ratios: ROE, ROCE, ROA when relevant
- Segment performance, order book, AUM, loan book, NPA, same-store sales, or other sector-specific metrics

## Analysis Framework

- **Growth:** revenue, profit, EPS, and volume growth. Separate organic growth from one-offs.
- **Margins:** expansion/compression drivers, sustainability, raw-material or pricing pressure.
- **Balance sheet:** debt load, interest coverage, cash, leverage, contingent liabilities.
- **Cash flow quality:** CFO vs PAT, free cash flow, receivables, inventory, capex intensity.
- **Working capital health:** debtor days vs creditor days vs inventory days (cash conversion cycle). Flag if working capital is expanding while profits grow — a classic cash bleed. Also check if promoter advances or related-party receivables are growing faster than revenue.
- **Segment quality:** every segment must be checked independently. A holding company can mask a burning subsidiary behind a profitable-looking core. Flag any segment with negative margins or negative CFO.
- **Capital efficiency:** ROE/ROCE trend and whether reinvestment earns attractive returns.
- **Earnings quality:** one-time gains, accounting changes, receivables growth faster than sales, cash conversion weakness.
- **Management commentary:** guidance, demand outlook, risk statements, capex plans.

## Sector Metric Overrides

Do not rely on generic financial ratios alone. Check for sector-specific metrics first:

| Sector | Must-Check Metric | Why It Matters |
|--------|------------------|----------------|
| Banks / NBFCs | GNPA, NNPA, PCR, CD ratio, RoA | Asset quality drives long-term returns; NPA can be hidden |
| Mutual Funds / AMC | Quarterly AAUM, expense ratio, market share trend | Flows drive revenue more than market level |
| IT / Tech | Utilization, deal pipeline, offshore mix, USD revenue | Currency and utilization mask true growth |
| Pharma | USFDA 483 citations, ANDA pipeline, R&D % | Regulatory risk is binary, not gradual |
| Infrastructure / Construction | Order book quality, execution track record, working capital intensity | Revenue recognition is a common manipulation vector |
| Real Estate | pre-sales, collections, inventory, land bank cost | Recognized revenue ≠ cash collected |
| FMCG | Volume growth vs value growth, channel inventory | Sometimes the trade hides real demand weakness |

## Output

```markdown
## Financial Report Analysis
- Growth trend: ...
- Margin trend: ...
- Working capital: ...
- Segment quality: ...
- Balance sheet: ...
- Cash flow quality: ...
- Capital efficiency: ...
- Earnings quality: ...
- Sector health: ...
- Financial verdict: [Improving / Stable / Mixed / Deteriorating]
```

If fresh financials are unavailable, use the latest available period and label it clearly.
