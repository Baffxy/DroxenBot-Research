# Research Notes — DroxenBot

## Research Timeline

### Month 1–2 — Initial Exploration
The first prototype focused on detecting newly launched tokens using raw DEX data.

The system generated ~80 signals per day but with low precision (≈10–20%).

Key lessons:

• High noise in early-stage token data


• Need for stronger filtering mechanisms

### Month 3–5 — Filtering Improvements
New filters were introduced:

• Liquidity thresholds

• Holder distribution analysis

• Buy/Sell pressure ratio

Result:

• Significant reduction in low-quality signals

• Improved early detection reliability

### Month 6–7 — Behavioral Signal Integration

Smart wallet tracking and milestone detection were introduced.

Key observation:

Behavioral wallet accumulation often preceded large growth events.

### Month 8–9 — Optimization Phase
The scoring engine was redesigned and signal thresholds refined.

Final outcome:

• Signals reduced from ~80/day → 10–15/day

• Precision increased to ~70–80% hit rate

This iterative improvement demonstrates the importance of **signal filtering and feature engineering** in real-time financial environments.
