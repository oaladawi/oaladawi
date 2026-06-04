# Project 4 — Automated Stock Trading Bot (Python + Interactive Brokers)

**Type:** Personal project · **Role:** Sole builder · **When:** 2026 · **Stack:** Python 3.11 · ib_insync · Interactive Brokers API · AI-assisted watchlists

> *A self-directed project I built to connect my finance knowledge to real, automated execution. Figures and features below describe the system's design; I'd encourage reviewers to ask me to walk through the code live.*

---

## Problem Statement
I wanted to bridge the gap between analyzing markets and acting on them — to turn trading ideas into a disciplined, rules-based system that executes automatically and removes emotion from the loop.

## Objective
Build a fully automated trading bot that connects to a live brokerage account, pulls real-time data, generates a watchlist, and manages positions with strict risk controls — running on its own during market hours.

## Tools Used
- **Python 3.11**
- **ib_insync** (Pythonic wrapper for the Interactive Brokers API)
- **Interactive Brokers** live account for execution and market data
- Live **price and news** data feeds
- **AI-assisted watchlist generation** (using Claude to help rank/screen candidates)

## Methodology / How It Works
- **Connectivity:** connects programmatically to a live Interactive Brokers account through `ib_insync`.
- **Data ingestion:** pulls live price data and market news for the universe of interest.
- **Watchlist generation:** builds a dynamic watchlist each cycle, using AI assistance to screen and prioritize candidates.
- **Risk management:** every position is governed by **stop-loss and take-profit** logic so losses are capped and gains are locked in by rule, not by feeling.
- **Scheduling:** the bot runs on a fixed cycle (every few minutes) **during market hours only**, re-evaluating data and positions each pass.
- **Logging:** all trades and decisions are logged for later review and debugging.

## What It Demonstrates
- End-to-end systems thinking: data → signal → decision → execution → logging
- Real brokerage API integration (not a paper simulation framework)
- Disciplined **risk management** encoded as rules
- Practical Python engineering: scheduling, error handling, live data, state

## Key Takeaways
This project taught me that the hardest part of trading is not the idea — it's enforcing discipline consistently. Encoding stop-loss and take-profit rules into code made that discipline automatic. It also deepened my Python skills well beyond coursework: working with a live API, handling real-time data, and keeping a long-running process reliable.

> ⚠️ **Note:** This is a personal learning project involving real capital and real market risk. I treat it as an engineering and risk-management exercise, not as evidence of trading returns.

## Skills Demonstrated
Python · API integration (Interactive Brokers / ib_insync) · real-time data handling · automation & scheduling · risk management logic · systems design · logging & debugging
