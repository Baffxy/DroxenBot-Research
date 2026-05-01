# DroxenBot Architecture
## Overview

DroxenBot is a real-time AI-driven pipeline designed to discover newly launched Solana tokens and identify high-potential opportunities at their earliest stages.

The system is built as a multi-layer data pipeline that collects, filters, scores, and delivers actionable alerts to users.

### 1. External Data Sources

The bot continuously collects on-chain and market data from multiple providers:

• Birdeye API

• Dexscreener API

• Helius Webhooks

• Pump.fun token scanner

• Twitter/X social signals

These sources provide raw blockchain and market intelligence.

### 2. Data Collection Layer

Responsible for discovering new tokens and gathering raw metrics.

Main components:

• Token Discovery Engine

• Smart Wallet Tracker

• Market Data Fetcher

• Liquidity & Holder Scraper

This layer transforms raw external data into structured datasets.

### 3. Data Processing Layer

This stage cleans and filters the data to remove unsafe or low-quality tokens.

Key operations:

•Token filtering engine

•Risk checks (LP lock, ownership, bundle detection)

•Market metrics calculation

•Feature extraction pipeline

Only tokens that pass strict quality filters move forward.

### 4. Intelligence / AI Layer

This is the decision-making core of DroxenBot.

Components:

•Token scoring algorithm

•Trend detection engine

•Tier classification (Gold / Silver / Bronze)

•Momentum analyzer

This layer ranks tokens based on probability of strong market performance.

### 5. Storage & Caching Layer

The system stores and caches data for speed and reliability.

• PostgreSQL → historical token database

• Redis → price tracking and duplicate alert prevention

This ensures the bot never sends repeated alerts and can track token growth over time.

### 6. Alert & Delivery Layer

The final stage delivers insights to users.

Features:

• Telegram alert system

• Leaderboard generator

• Milestone tracker (2x, 3x, 5x, etc.)

Users receive real-time alerts for high-potential tokens.
