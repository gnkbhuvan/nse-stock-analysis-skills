# AI NSE Stock Analysis Skills

> Modular AI stock-analysis skills for NSE/BSE Indian equities. Give a stock name or symbol and get a complete research-style report covering business quality, financials, news, valuation, technicals, risks, investor mental models, and 1-year price scenarios.

**Zero hard dependencies.** The skills work with user-provided data, and become more powerful with live market data, public filings, company reports, and news sources.

## Install

Install all skills:

```bash
npx skills add gnkbhuvan/nse-stock-analysis-skills --skill '*'
```

Install only the main stock analysis skill:

```bash
npx skills add gnkbhuvan/nse-stock-analysis-skills --skill stock-analysis
```

Install only the NSE multibagger skill:

```bash
npx skills add gnkbhuvan/nse-stock-analysis-skills --skill nse-multibagger
```

List available skills before installing:

```bash
npx skills add gnkbhuvan/nse-stock-analysis-skills --list
```

Skills live under `skills/<skill-name>/SKILL.md`, the standard layout used by the Skills CLI and skills.sh discovery.

## What These Skills Do

These skills turn an AI agent into an Indian equity research assistant. The default workflow is:

1. Resolve the stock name or symbol.
2. Fetch or request price, company, financial, news, and technical data.
3. Analyze business quality, financial performance, valuation, technical setup, red flags, and investor quality.
4. Build 1-year bull/base/bear price scenarios.
5. Produce an educational AI view with confidence, key triggers, invalidation points, and a short investor-style one-liner.

## Skills Included

| # | Skill | What It Does |
|---|-------|-------------|
| 1 | **stock-analysis** | Master orchestrator for complete NSE/BSE stock research reports |
| 2 | **stock-profile** | Company identity, business model, moat, sector, and competitive position |
| 3 | **news-analysis** | Recent news, filings, announcements, corporate actions, and sentiment impact |
| 4 | **financial-report-analysis** | Quarterly/annual financials, margins, cash flow, debt, and earnings quality |
| 5 | **valuation-analysis** | Valuation ratios, peer comparison, historical valuation, and margin of safety |
| 6 | **technical-analysis** | Weekly/daily chart structure, indicators, support/resistance, and key levels |
| 7 | **scenario-forecasting** | 1-year bull/base/bear stock-price ranges with assumptions |
| 8 | **investor-checklist** | Quality + value mental models inspired by public principles of great investors |
| 9 | **red-flag-analysis** | Governance, debt, valuation, earnings, sector, liquidity, and technical risks; includes India-specific hard triggers (promoter pledge threshold, auditor qualifications, ICR, CFO/PAT ratio) |
| 10 | **final-recommendation** | Final rating, confidence, action zone, thesis, invalidation, and one-liner |
| 11 | **nse-multibagger** | Peter Lynch-style screen for undervalued high-growth NSE multibagger candidates; includes India-specific hard filters (promoter pledge, auditor issues, debt/EBITDA, liquidity) |

## Usage Examples

```text
"Analyze RELIANCE completely"
"Give me a full NSE stock report for TATAMOTORS"
"What is the 1-year upside/downside for INFY?"
"Assess DMART like a long-term investor"
"Check if SBIN is worth holding from here"
"What can go wrong with ZOMATO stock?"
"Give me a Jhunjhunwala/Damani-style one-line view on HDFCBANK"
"Find NSE multibagger stocks"
"Screen undervalued high-growth NSE stocks"
"Analyze CDSL like Peter Lynch"
"Give me top 10 NSE multibagger candidates"
```

## Data Sources

The skills can operate in two modes:

### Enhanced Mode

Use available tools such as:

- Groww MCP for symbol lookup, live quotes, depth, holdings, indicators, and candles
- yfinance-style historical data for OHLCV and long-term price history
- NSE/BSE/company investor-relations pages for filings, annual reports, results, and corporate actions
- Reliable business news sources for recent events

### Manual Mode

If live tools are unavailable, provide:

- stock name/symbol
- current price
- recent financials or report snippets
- recent news
- chart levels or technical indicator values

The agent should clearly state what data is missing and reduce confidence where needed.

## Default Report Template

```markdown
# [STOCK] Complete NSE Stock Analysis - [Date]

## Quick View
[Rating, confidence, 1-year view, top reason, top risk]

## Data Quality
[Sources used, missing data, freshness, confidence]

## Stock Identity
[Company, symbol, sector, market cap, price, liquidity]

## Business Profile
[Business model, revenue drivers, moat, competition, sector context]

## News & Events
[Latest developments, filings, corporate actions, sentiment, impact]

## Financial Report Analysis
[Growth, margins, debt, cash flow, ROE/ROCE, earnings quality]

## Valuation
[Ratios, peers, history, margin of safety, valuation judgment]

## Technical View
[Trend, support/resistance, indicators, volume, key levels]

## 1-Year Price Outlook
| Scenario | Price Range | Upside/Downside | Assumptions | Trigger | Invalidation |
|----------|-------------|-----------------|-------------|---------|--------------|

## Investor Quality Checklist
[Quality + value assessment]

## Risks & Red Flags
[Risk score and key risks]

## Final AI View
[Rating, thesis, action zone, invalidation, top 3 risks]

> Investor-style one-liner: [Jhunjhunwala-style or Damani-style one-line view]
```

## Investor Mental Models

The toolkit uses public principles associated with great investors. It must not claim to quote or represent any investor personally. When these principles appear in analysis output, they are educational shorthand — summaries of well-known public investing frameworks, not personal endorsements or exact quotes from any investor.

- **Jhunjhunwala-style:** opportunity size, earnings growth, promoter quality, sector tailwind, conviction.
- **Damani-style:** simple business, cash generation, valuation comfort, downside protection, patience.
- **Buffett/Munger-style:** durable moat, honest management, pricing power, ROE/ROCE, low debt.
- **Peter Lynch-style:** understandable story, visible growth, reasonable valuation.
- **Graham-style:** margin of safety and downside protection.
- **Howard Marks-style:** cycle risk, sentiment, probabilities, and downside awareness.

## NSE Multibagger Screen

Use **nse-multibagger** when the user asks for multibagger ideas, undervalued high-growth stocks, Peter Lynch-style analysis, or top NSE candidates.

> **Attribution note:** "Peter Lynch-style" is public investing-principle shorthand. It does not claim to quote or represent Peter Lynch personally. Do not use it as an endorsement or exact recommendation from any investor.

Default behavior:

- Screen NSE 500 plus smaller midcap/smallcap names that pass liquidity and governance filters
- Prefer quality-first candidates over cheap value traps
- Rank the top 10 ideas using growth, quality, valuation, technical, and risk scores
- Deep dive the best candidates with 3-5 year scenarios, thesis breakers, and worst-case analysis
- Classify each idea with a Peter Lynch-style lens: fast grower, stalwart, turnaround, cyclical, asset play, or slow grower

Example output:

```markdown
# NSE Multibagger Screen - [Date]

## Top 10 Candidates
| Rank | Stock | Lynch Type | Growth | Quality | Valuation | Technical | Risk | Verdict |

## Deep Dive: [Best Candidate]
- Business story: ...
- Peter Lynch classification: ...
- 3-5 year bull/base/bear scenarios: ...
- Worst-case scenario: ...
- Thesis breakers: ...
- Position risk label: [Core / Satellite / Speculative / Avoid]
- Final view: ...

## Avoid / Watchlist Names
[Stocks rejected or kept on watchlist and why]

> Lynch-style one-liner: [simple one-line explanation]
```

## Rating Scale

Full definitions are in the `final-recommendation` skill. Summary:

| Rating | Meaning |
|--------|---------|
| Strong Buy | High-quality setup with attractive valuation and strong evidence |
| Buy on Dips | Good business, but entry price matters |
| Accumulate | Add gradually when valuation or technical levels are favorable |
| Hold | Existing holders can continue, but new entry is not compelling |
| Watchlist | Interesting, but wait for trigger, better valuation, or cleaner data |
| Avoid | Risk/reward is unattractive |
| Reduce / Exit | Thesis has weakened or downside risk dominates |

## Disclaimer

These skills are educational tools for stock analysis. They do not constitute financial advice, investment advice, or a guarantee of returns. Always do your own research and consult a qualified financial advisor before investing.

## Acknowledgements

This project was inspired by the original [Bhala-Srinivash/nse-trading-skills](https://github.com/Bhala-Srinivash/nse-trading-skills) repository by Bhala Srinivash. That work focused on NSE/BSE trading-analysis skills; this repo expands the idea into a broader AI stock-analysis toolkit with fundamentals, valuation, news, technicals, risk analysis, investor mental models, and NSE multibagger screening.

## License

MIT. The original project was also MIT licensed; this revamped version keeps the same permissive license while preserving attribution.
