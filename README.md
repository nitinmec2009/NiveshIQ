<p align="center">
  <img src="assets/logo.png" alt="NiveshIQ Logo" width="120" />
</p>

# NiveshIQ — AI Market Intelligence for Indian Stocks (NSE)

Turns real-time market news + price data into simplified explanations and **expected-move signals (1D/1W/1M)** for **retail investors and students**. :contentReference[oaicite:3]{index=3}

> **Disclaimer:** NiveshIQ is for educational purposes only and does not constitute investment advice. AI can make errors; users should use their discretion before trading or investing. :contentReference[oaicite:4]{index=4}

---

## What is NiveshIQ?

**NiveshIQ** is a market intelligence platform purpose-built for the **Indian stock market (NSE)**. It helps users answer: :contentReference[oaicite:5]{index=5}

- **Why did this stock/sector move today?**
- **What might move next — and why?**
- **What is the expected move (1D/1W/1M) with confidence?**

Instead of raw headlines, NiveshIQ produces **structured insights**, **impact classification**, and **easy-to-understand reasons**. :contentReference[oaicite:6]{index=6}

---

## The Problem

Retail investors often struggle to: :contentReference[oaicite:7]{index=7}

- Interpret financial news quickly  
- Connect macro events (crude, USD/INR, yields) to sectors/stocks  
- Understand whether a headline is **material** or noise  
- Quantify possible impact and react in time  

Most end up relying on social media tips, delayed analysis, or fragmented tools. :contentReference[oaicite:8]{index=8}

---

## The Solution

NiveshIQ combines: :contentReference[oaicite:9]{index=9}

- **Real-time news ingestion** (RSS + headline sources)
- **Fast sentiment scoring** (FinBERT)
- **LLM-based reasoning + structuring** (Ollama / cloud LLMs)
- **Multi-factor expected-move model**
- **Web + Mobile UX** with heatmaps, dashboards, and watchlists

---

## Key Capabilities

- Tracks **~750+ NSE stocks** (Nifty Total Market universe) :contentReference[oaicite:10]{index=10}  
- Heatmaps across **sectors, market-cap, and themes** (42 indices) :contentReference[oaicite:11]{index=11}  
- **High Impact dashboard**: top gainers/losers, expected movers, volume spikes :contentReference[oaicite:12]{index=12}  
- **Stock deep-dive page**: news, signals, explanations, confidence :contentReference[oaicite:13]{index=13}  
- Personal **watchlist** with alerts-ready structure :contentReference[oaicite:14]{index=14}  
- AI market assistant chat for user questions :contentReference[oaicite:15]{index=15}  
- Multi-language UI (11 Indian languages) :contentReference[oaicite:16]{index=16}  

---

## Product Screens

<p align="center">
  <img src="assets/screenshots/main_page.png" width="45%" />
  <img src="assets/screenshots/market_heatmap_market_cap.png" width="45%" />
</p>
<p align="center">
  <img src="assets/screenshots/stock_comprehensive.png" width="45%" />
  <img src="assets/screenshots/thematic_constituents.png" width="45%" />
</p>

> Tip: If you create a short demo video (30–60s), add it here as a “Demo” link for AWS Activate reviewers.

---

## How It Works (High-Level)

### Data + AI Pipeline

1. **Ingest news** (RSS / headlines) and **deduplicate** :contentReference[oaicite:17]{index=17}  
2. **FinBERT** scores sentiment (positive/neutral/negative) :contentReference[oaicite:18]{index=18}  
3. **LLM** generates structured output:
   - symbols/entities  
   - topics  
   - impact level (high/medium/low)  
   - short reasoning summary :contentReference[oaicite:19]{index=19}  
4. Merge with market data and calculate:
   - trend + momentum  
   - sentiment windows  
   - volatility normalization :contentReference[oaicite:20]{index=20}  
5. Publish to dashboards/stock pages with caching for fast load :contentReference[oaicite:21]{index=21}  

### Performance Principle (for fast loading)
- **AI and ingestion run in background jobs**
- APIs serve **precomputed results** from DB/cache  
This avoids doing heavy AI work on page load.

---

## Expected Move (Model Summary)

NiveshIQ uses a multi-factor model to estimate **expected move** and confidence. :contentReference[oaicite:22]{index=22}

Example factors: :contentReference[oaicite:23]{index=23}
- Momentum  
- Trend  
- Short-term sentiment (24h)  
- Medium-term sentiment (7d)  
- Volatility normalization  

Outputs are capped to avoid extreme values and are presented as:
- **1D / 1W / 1M expected move**
- **confidence**
- **plain-English explanation** :contentReference[oaicite:24]{index=24}  

---

## Planned AWS Deployment (for AWS Activate)

NiveshIQ needs scalable, reliable infrastructure for: :contentReference[oaicite:25]{index=25}  
- Continuous ingestion + scheduled pipelines  
- AI processing workloads (batch + near-real-time)  
- Low-latency APIs for web and mobile  
- Secure user authentication and data storage  
- Monitoring and cost control  

### AWS Services (Planned) :contentReference[oaicite:26]{index=26}
- **Amazon ECS (or EC2)** — API + worker services  
- **Amazon RDS (PostgreSQL)** — production DB for news, tags, rollups, users  
- **Amazon ElastiCache (Redis)** — caching hot endpoints (heatmaps, stock pages)  
- **Amazon S3** — raw news archives, model artifacts, static assets/screenshots  
- **AWS Lambda** — lightweight background jobs (scheduled tasks, triggers)  
- **Amazon CloudWatch** — logs, alarms, monitoring  
- **API Gateway / ALB** — routing and security controls  

### Social Feed add-on (planned on AWS)
- **S3 + CloudFront** for media (images/videos)
- **RDS + Redis** for posts/comments/likes + trending ranking
- Optional: **Amazon Cognito** for user authentication

---

## Current Stage

- Prototype and core pipelines implemented (news ingestion + AI tagging + dashboards) :contentReference[oaicite:27]{index=27}  
- Web dashboard working in development :contentReference[oaicite:28]{index=28}  
- Mobile app in progress :contentReference[oaicite:29]{index=29}  
- Preparing for beta launch and early user onboarding :contentReference[oaicite:30]{index=30}  

---

## Roadmap

### Near-term (0–2 months)
- Portfolio tracking and P&L analytics :contentReference[oaicite:31]{index=31}  
- Better onboarding and personalization :contentReference[oaicite:32]{index=32}  
- Push notifications for watchlist (news + signal triggers) :contentReference[oaicite:33]{index=33}  
- Improve caching + precomputed rollups for faster stock/global pulse pages

### Next (2–4 months)
- Real-time price updates (WebSockets) :contentReference[oaicite:34]{index=34}  
- Options / implied volatility overlays :contentReference[oaicite:35]{index=35}  
- Broker integrations (order-routing optional) :contentReference[oaicite:36]{index=36}  
- Backtesting + model calibration :contentReference[oaicite:37]{index=37}  

---

## Community Roadmap: Reddit-style Financial Social Feed

Goal: make NiveshIQ a **financial social app** where users learn markets through **news-driven discussions, memes, and short videos** — targeting **retail investors + students**.

### Phase 1 (MVP): Channels + Posts + Comments
- Create/join **Channels** (e.g., #Nifty, #BankNifty, #IPOs, #LongTerm, #Beginner, #Memes)
- Post **text / image / video** with optional tags: `stock`, `sector`, `theme`, `news-link`
- **Like / comment / reply threads**
- Sort: **Trending / Latest / Top (24h / 7d)**
- Basic moderation: report, block, remove post (admin/mod roles)

### Phase 2: News → Social loop + Safety
- Auto-generate “Top Stories” post per channel (from Global Pulse)
- Meme/video generation workflow (human review first)
- Reputation/karma + badges (Beginner, Analyst, Trader)
- Anti-spam + rate limits + toxicity filter + duplicate detection

### Phase 3: Growth + Monetization (optional)
- Premium/private channels
- Clearly-labeled sponsored learning series
- Creator tools + analytics
- Verified expert Q&A sessions

---

## Repository Note (Public README)

This repository is a **public product overview** for demos, architecture, and AWS Activate evaluation. :contentReference[oaicite:38]{index=38}  
The production source code is maintained separately in a private repository. :contentReference[oaicite:39]{index=39}  

---

## Founder / Co-Founder

- **Nitin Agarwal** — Investment Banking :contentReference[oaicite:40]{index=40}  
- **Sanskriti Garg** — DevOps + AI systems engineering; scalable pipelines, deployment automation, production-ready infra :contentReference[oaicite:41]{index=41}  

---

## Contact

- Email: sanskritigarg31@gmail.com :contentReference[oaicite:42]{index=42}  
- LinkedIn: https://www.linkedin.com/in/sanskriti-garg-0407 :contentReference[oaicite:43]{index=43}  
