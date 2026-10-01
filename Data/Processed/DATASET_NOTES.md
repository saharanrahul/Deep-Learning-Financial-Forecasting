# Dataset Notes -- auto-generated 2026-10-01 08:00

## Survivorship bias: what this notebook did and did not fix

- **Universe expanded** using the free, community-maintained historical
  constituent list from github.com/fja05680/sp500 (coverage: 1996 onward).
- Currently-listed tickers attempted: 503, succeeded: 464 (92.2%).
- Historical-only (delisted/renamed/acquired) tickers attempted: 647, succeeded: 145 (22.4%).
- **Interpretation:** the gap between these two success rates is the honest
  measure of how much this free-data approach can recover. A large gap
  means most delisted-company price history remains unavailable without a
  paid source (CRSP, Bloomberg, WRDS) -- this is expected and documented,
  not a bug.

## Remaining limitations (unchanged / restated)

1. **Pre-1996 delistings are still missing entirely** (no free source found
   for 1990-1996 index membership changes).
2. Historical constituent membership for 1996-2001 is described by the
   source's own maintainer as potentially incomplete.
3. Price/return variable, corporate actions, valuation variables, and risk
   factors: same status as documented in the original Notebook 1 run.
