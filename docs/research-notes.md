# Research Notes — DroxenBot

## Research Timeline

### Month 1–2 — Initial Exploration

The first prototype focused on detecting newly launched tokens using raw DEX data.

The system generated ~80 signals per day but with low precision (≈10–20%).

Key lessons:

- High noise in early-stage token data
  
- Need for stronger filtering mechanisms

### Month 3–5 — Filtering Improvements

New filters were introduced:

- Liquidity thresholds
  
- Holder distribution analysis
  
- Buy/Sell pressure ratio

Result:

- Significant reduction in low-quality signals
  
- Improved early detection reliability

### Month 6–7 — Behavioral Signal Integration

Smart wallet tracking and milestone detection were introduced.

Key observation: behavioral wallet accumulation often preceded large growth events.

### Month 8–9 — Optimization Phase

The scoring engine was redesigned and signal thresholds refined.

Final outcome:

- Signals reduced from ~80/day to 10–15/day
  
- Observed hit rate increased to ~70–85%

*As with all figures in this document, these are drawn from continuous hands-on observation during deployment rather than a fixed, consistently-applied success threshold or a baseline comparison — see the accompanying research paper's Measurement Methodology (Section 4.5) and Limitations (Section 5.4) for full detail.*

This iterative improvement demonstrates the importance of signal filtering and feature engineering in real-time financial environments.
