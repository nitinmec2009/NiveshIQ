<p align="center">
  <img src="assets/logo.png" alt="NiveshIQ Logo" width="90" />
</p>

<h1 align="center">NiveshIQ — AI Market Intelligence for Indian Stocks</h1>

<p align="center">
  <strong>Turns real-time market news + price data into simplified explanations and expected-move signals for retail investors.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Market-NSE%20India-blue" />
  <img src="https://img.shields.io/badge/AI-FinBERT%20%2B%20LLM-orange" />
  <img src="https://img.shields.io/badge/Web-Next.js-black?logo=nextdotjs" />
  <img src="https://img.shields.io/badge/API-FastAPI-009688?logo=fastapi" />
  <img src="https://img.shields.io/badge/DB-PostgreSQL-336791?logo=postgresql" />
  <img src="https://img.shields.io/badge/Cache-Redis-D82C20?logo=redis" />
</p>

---

## What is NiveshIQ?

**NiveshIQ** is a market intelligence platform purpose-built for the **Indian stock market (NSE)**.

It helps investors answer:
- **Why did this stock/sector move today?**
- **What might move next — and why?**
- **What is the expected move (1D/1W/1M) with confidence?**

Instead of raw headlines, NiveshIQ produces **structured insights**, **impact classification**, and **easy-to-understand reasons**.

---

## The Problem

Retail investors often struggle to:
- Interpret financial news quickly
- Connect macro events (crude, USD/INR, yields) to sectors/stocks
- Understand whether a headline is **material** or just noise
- Quantify possible impact and react in time

Most end up relying on social media tips, delayed analysis, or fragmented tools.

---

## The Solution

NiveshIQ combines:
- **Real-time news ingestion** (RSS + headlines sources)
- **Fast sentiment scoring** (FinBERT)
- **LLM-based reasoning and structuring** (Ollama / cloud LLMs)
- **Multi-factor expected-move model**
- **Web + Mobile UX** with heatmaps, dashboards, and watchlists

---

## Key Capabilities

- **Tracks ~750+ NSE stocks** (Nifty Total Market universe)
- **Heatmaps** across **sectors, market-cap, and themes** (42 indices)
- **High Impact dashboard**: top gainers/losers, expected movers, volume spikes
- **Stock deep-dive page**: news, signals, explanations, and confidence
- **Personal watchlist** with alerts-ready structure
- **AI market assistant chat** for user questions
- **Multi-language UI** (11 Indian languages)

> Note: NiveshIQ is for educational purposes only and does not constitute investment advice. AI can make errors; users should use their discretion before trading or investing.

---

## Product Screens (Add screenshots)

Add screenshots in `/assets/screenshots/` and update the links below:

<p align="center">
  <img src="assets/screenshots/global-pulse.png" width="30%" />
  <img src="assets/screenshots/market-heatmap.png" width="30%" />
  <img src="assets/screenshots/stock-page.png" width="30%" />
</p>

---

## How It Works (High-Level)

### Data + AI Pipeline

1. **Ingest news** (RSS / headlines) and **deduplicate**
2. **FinBERT** scores sentiment (positive/neutral/negative)
3. **LLM** generates structured output:
   - symbols/entities
   - topics
   - impact level (high/medium/low)
   - short reasoning summary
4. **Merge with market data** and calculate:
   - trend + momentum
   - sentiment windows
   - volatility normalization
5. Publish to dashboards and stock pages with caching for fast load

---

## Expected Move (Model Summary)

NiveshIQ uses a multi-factor model to estimate **expected move** and confidence.

Example factors:
- Momentum
- Trend
- Short-term sentiment (24h)
- Medium-term sentiment (7d)
- Volatility normalization

Outputs are capped to avoid extreme values and are presented as:
- **1D / 1W / 1M expected move**
- **confidence**
- **plain-English explanation**

---

## Planned AWS Deployment (for AWS Activate)

NiveshIQ needs scalable, reliable infrastructure for:
- Continuous ingestion + scheduled pipelines
- AI processing workloads (batch + near-real-time)
- Low-latency APIs for web and mobile
- Secure user authentication and data storage
- Monitoring and cost control

### AWS Services (Planned)

- **Amazon ECS (or EC2)** — API + worker services
- **Amazon RDS (PostgreSQL)** — production database for news, tags, rollups, users
- **Amazon ElastiCache (Redis)** — caching hot endpoints (heatmaps, stock pages)
- **Amazon S3** — raw news archives, model artifacts, static assets/screenshots
- **AWS Lambda** — lightweight background jobs (scheduled tasks, triggers)
- **Amazon CloudWatch** — logs, alarms, monitoring
- **API Gateway / ALB** — routing and security controls

---

## Current Stage

- Prototype and core pipelines implemented (news ingestion + AI tagging + dashboards)
- Web dashboard working in development
- Mobile app in progress
- Preparing for beta launch and early user onboarding

---

## Roadmap

**Near-term**
- Portfolio tracking and P&L analytics
- Better onboarding and personalization
- Push notifications for watchlist (news + signal triggers)

**Next**
- Real-time price updates (WebSockets)
- Options / implied volatility overlays
- Broker integrations (order-routing optional)
- Backtesting + model calibration

---

## Repository Note (Public README)

This repository is a **public product overview** for demos, architecture, and AWS Activate evaluation.

The production source code is maintained separately in a private repository.

---

## Founder

**Sanskriti Garg**  
DevOps + AI systems engineering background  
Building scalable pipelines, deployment automation, and production-ready infra.

---

## Contact

- Email: your@email.com
- LinkedIn: https://www.linkedin.com/in/yourprofile/

---

