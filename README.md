# DroxenBot: A Real-Time Autonomous Agent for On-Chain Detection and Ranking of Emerging Digital Assets

### Research Project Repository

**Author:** Abdullahi Labaran  
**Background:** B.Tech Computer Engineering (AI & Data Science)  
**Research Interests:** Autonomous Systems, Machine Learning, Modeling & Simulation  
**Email:** baffahlabaran01@gmail.com                                                           
**LinkedIn:** www.linkedin.com/in/abdullahi-labaran                                                                                      
**Year:** 2026

> **Implementation note:** This public repository documents the research
> design, architecture, and experimental evolution of DroxenBot. The
> full production implementation (data pipelines, real-time monitoring
> services, deployment configuration, and proprietary filtering/scoring
> logic) is maintained in a private repository, since the system
> underlies a live, commercially operating product. Access to the full
> implementation can be provided to academic reviewers upon request.

## Abstract

DroxenBot is an experimental autonomous market-intelligence agent designed to monitor and rank emerging digital assets using real-time on-chain activity, decentralized-exchange market data, and behavioral wallet signals.

The system combines decentralized exchange analytics, blockchain data streams, and rule-based heuristic scoring to identify emerging assets before major price discovery occurs.

This project explores how **autonomous decision systems** can operate continuously in noisy, high-velocity financial environments.

## Research Motivation

Unlike traditional financial markets, decentralized markets are:

- Real-time
- Noisy and unstructured
- Highly volatile
- Dominated by behavioral signals

Early detection of promising assets requires autonomous systems capable of:

- Continuous monitoring
- Noise filtering
- Opportunity ranking
- Real-time reaction under uncertainty

DroxenBot investigates how **rule-based autonomous agents** can operate in such environments.

## Research Questions

This project explores:

1. Can algorithmic filters detect promising assets earlier than human traders?
   
2. Which on-chain signals correlate with large market movements?
   
3. Can smart-wallet behavior serve as a predictive feature?
   
4. How can autonomous agents reduce noise in speculative markets?

## Key Contributions

This project contributes the following:

- Design of a real-time autonomous monitoring pipeline for decentralized markets
  
- Development of a multi-stage token filtering and ranking system
  
- Empirical observation of behavioral wallet activity as an early signal
  
- Iterative optimization improving observed signal hit rate from ~10-20% to ~70-85% (see caveats below)
  
- Deployment of a live production system delivering real-time alerts to real subscribers

## System Architecture

### Agent Pipeline

**Token Discovery** — monitor newly launched tokens; track trending assets across DEX markets

**Data Aggregation** — liquidity depth, market cap & volume velocity, transaction activity, smart wallet accumulation, holder distribution

**Filtering Engine** — removes high-risk or low-quality tokens using rule-based filters

**Scoring Engine** — ranks tokens into tiers: Bronze (early signal) → Silver (strong momentum) → Gold (high-confidence trend)

**Real-Time Alerts** — automated alert system for newly detected signals and growth milestones

![Architecture](https://github.com/Baffxy/DroxenBot-Research/raw/main/docs/architecture.png)

The diagram above shows the end-to-end pipeline of DroxenBot.

## Live Deployment

The system has been deployed as a production Telegram bot and has been operating continuously in real market conditions.

Over the research period:

- ~9 months of continuous monitoring
- Thousands of tokens analyzed
- Real users subscribed to alerts
- Ongoing performance tracking of detected assets

## Experimental Evolution

The system was iteratively improved over a **9-month research period**.

| Phase            | Signals / Day | Hit Rate |
| ---------------- | ------------- | -------- |
| Early Prototype  | 80            | 10–20%   |
| Optimized System | 10–15         | 70–85%   |

*These hit-rate figures come from continuous hands-on observation during deployment — cross-referenced against automated tracking and real-time public documentation of calls at [x.com/Droxenbot](https://x.com/Droxenbot) — not from a fixed, consistently-applied success threshold or a controlled baseline comparison.See the accompanying research paper's Measurement Methodology section for full detail, and its Limitations section for what a more rigorous evaluation would require.*

## Technical Stack

| Component       | Technology         |
| --------------- | ------------------ |
| Language        | Python              |
| Backend         | FastAPI             |
| Database        | PostgreSQL          |
| Cache           | Redis               |
| Blockchain Data | Helius API          |
| Market Data     | DEX Analytics APIs  |
| Deployment      | Railway / Render    |

## Repository Structure

This public repository contains the research documentation and architecture design, not the full production codebase (see implementation note above):

```
DroxenBot-Research/
│
├── docs/                # Architecture diagram and supplementary documentation
│   └── architecture.png
├── src/                 # Notice pointing to the private implementation repository
├── README.md
├── LICENSE
└── requirements.txt
```

The full production system is organized internally as data collection, filtering, scoring, storage, and alerting layers shown conceptually in the architecture diagram above — but that code is not part of this public repository.

## Methodology

### Feature Engineering Signals

The system evaluates assets using:

- Liquidity depth
- Buy/Sell pressure ratio
- Volume growth rate
- Holder concentration
- Smart wallet accumulation
- Time since launch
- Market cap momentum

### Scoring Strategy

Weighted heuristic model combining **market metrics + on-chain signals + behavioral indicators**.

## Research Relevance

This work connects to research areas in:

- Autonomous Agents
- Real-Time Systems
- Modeling & Simulation
- Multi-Agent Decision Systems
- Data-Driven Forecasting

### Key Observations

- Signal filtering meaningfully improved observed hit rate over time, by the author's continuous hands-on tracking
- Behavioral wallet accumulation was frequently observed preceding major growth events among tokens later flagged as successful
- Early-stage assets exhibit measurable momentum patterns detectable via real-time data streams

These are observational findings from live deployment, not statistically validated causal claims — they motivate the more rigorous evaluation protocol and baseline comparisons proposed below and detailed in the accompanying paper.

## Future Research Directions

1. **Rigorous Evaluation Protocol** — a fixed, pre-registered success threshold applied consistently to every detection, with proper precision/recall/F1 reporting
2. **Baseline Comparisons** — against random selection and simple single-metric filters, to isolate the actual contribution of the multi-stage architecture
3. **Machine-Learning Ranking** — training supervised/semi-supervised models on accumulated detection history, compared against the current heuristic scorer
4. **Temporal and Graph-Based Modeling** — representing wallet and transaction relationships as temporal graphs
5. **Simulation and Backtesting** — controlled environments that replay historical streams
6. **Cross-Chain Generalization** — extending to additional blockchain ecosystems
7. **Risk-Aware Decision Support** — incorporating explicit uncertainty and liquidity constraints
8. **Autonomous Execution as a Separate Research Problem** — evaluated independently under controlled risk limits, not conflated with monitoring performance

This project serves as a foundation for future research into autonomous decision systems in real-time financial environments.

## Paper

The full research paper — including detailed methodology, honest discussion of measurement limitations, and results — is available as a preprint: *[link to be added once posted to arXiv]*.

## Disclaimer

This project is for research and educational purposes only and does not constitute financial advice. Speculative digital-asset markets carry substantial financial risk independent of any detection system's performance.
