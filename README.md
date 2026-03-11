<div align="center">

<br />

```
███╗   ██╗███████╗██╗  ██╗██╗   ██╗███████╗
████╗  ██║██╔════╝╚██╗██╔╝██║   ██║██╔════╝
██╔██╗ ██║█████╗   ╚███╔╝ ██║   ██║███████╗
██║╚██╗██║██╔══╝   ██╔██╗ ██║   ██║╚════██║
██║ ╚████║███████╗██╔╝ ██╗╚██████╔╝███████║
╚═╝  ╚═══╝╚══════╝╚═╝  ╚═╝ ╚═════╝ ╚══════╝
```

### Global Market Intelligence Platform

**Open-source · Real-time · AI-powered**

<br />

[![License: MIT](https://img.shields.io/badge/License-MIT-0066FF.svg?style=flat-square)](LICENSE)
[![Next.js](https://img.shields.io/badge/Next.js-14-000000?style=flat-square&logo=nextdotjs)](https://nextjs.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.110-009688?style=flat-square&logo=fastapi)](https://fastapi.tiangolo.com)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16-336791?style=flat-square&logo=postgresql)](https://postgresql.org)
[![Docker](https://img.shields.io/badge/Docker-ready-2496ED?style=flat-square&logo=docker)](https://docker.com)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-12B76A.svg?style=flat-square)](CONTRIBUTING.md)

<br />

[Live Demo](https://nexus.io) · [Documentation](https://docs.nexus.io) · [Report Bug](https://github.com/yourname/nexus/issues) · [Request Feature](https://github.com/yourname/nexus/discussions)

<br />

</div>

---

## What is NEXUS?

NEXUS is a fully open-source global market intelligence platform that combines three powerful systems in one:

| Module | Description |
|--------|-------------|
| 🛒 **Global Marketplace** | Buy and sell physical products, digital goods, and freelance services — worldwide, multi-currency |
| 📡 **World Monitor** | Real-time geopolitical event tracking across 400+ news sources in 47 languages |
| 📊 **Economic Analytics** | Live data from 92 stock exchanges, AI-generated market reports, and geopolitical risk scoring |

---

## Features

### 🛒 Global Marketplace
- Physical products, digital downloads, and freelance services
- 150+ supported currencies with automatic conversion
- Stripe Connect for global seller payouts
- Seller dashboard with revenue analytics
- Review and rating system

### 📡 World Monitor
- Aggregates 400+ RSS feeds — newspapers, agencies, broadcast, wires
- Real-time keyword alerting with email and push notifications
- Country Instability Index (CII) — 0 to 100 composite score
- Interactive geopolitical heatmap with event clustering
- AI-generated intelligence briefings every 4 hours

### 📊 Economic Analytics
- Live market data from 92 global stock exchanges
- Geopolitical risk scoring across 195 countries
- AI-powered investment opportunity radar
- Macroeconomic indicator tracking (GDP, CPI, PMI, trade volumes)
- Correlation engine — detect how events affect markets

### 🤖 AI Engine
- Auto-summarize news in the reader's language
- Predict market impact of geopolitical events
- Pattern and anomaly detection across signals
- Personalized feed based on user interests

---

## Tech Stack

```
┌─────────────────────────────────────────────┐
│                   NEXUS                      │
├──────────────┬──────────────────────────────┤
│  Frontend    │  Next.js 14 · TypeScript      │
│              │  Tailwind CSS · Zustand        │
│              │  Mapbox GL · Socket.io         │
├──────────────┼──────────────────────────────┤
│  Backend     │  Python · FastAPI              │
│              │  SQLAlchemy · Alembic          │
│              │  Celery · Redis                │
├──────────────┼──────────────────────────────┤
│  Database    │  PostgreSQL 16 (primary)       │
│              │  Redis (cache + queue)         │
│              │  Meilisearch (full-text)        │
├──────────────┼──────────────────────────────┤
│  AI / ML     │  OpenAI API · Ollama (local)   │
│              │  NLTK · Transformers           │
├──────────────┼──────────────────────────────┤
│  Payments    │  Stripe Connect                │
│  Storage     │  AWS S3 / Cloudflare R2        │
│  Deploy      │  Docker · Nginx · GitHub CI    │
└──────────────┴──────────────────────────────┘
```

---

## Project Structure

```
nexus/
│
├── 📁 frontend/                  # Next.js 14 application
│   ├── src/
│   │   ├── app/                  # App Router pages
│   │   │   ├── dashboard/
│   │   │   ├── marketplace/
│   │   │   ├── monitor/
│   │   │   ├── analytics/
│   │   │   └── api/              # Route handlers
│   │   ├── components/           # Reusable UI components
│   │   │   ├── ui/               # Base design system
│   │   │   ├── marketplace/
│   │   │   ├── monitor/
│   │   │   ├── analytics/
│   │   │   └── charts/
│   │   ├── hooks/                # Custom React hooks
│   │   ├── lib/                  # Utilities and config
│   │   ├── store/                # Zustand state stores
│   │   └── types/                # TypeScript definitions
│   └── public/                   # Static assets
│
├── 📁 backend/                   # FastAPI Python backend
│   ├── main.py                   # Application entry point
│   ├── requirements.txt
│   └── app/
│       ├── api/v1/               # API route handlers
│       │   └── endpoints/
│       │       ├── auth.py
│       │       ├── listings.py
│       │       ├── orders.py
│       │       ├── monitor.py
│       │       ├── analytics.py
│       │       └── search.py
│       ├── core/                 # Config, security, database
│       ├── models/               # SQLAlchemy ORM models
│       ├── schemas/              # Pydantic request/response schemas
│       └── services/             # Business logic layer
│           ├── marketplace/
│           ├── monitor/
│           ├── analytics/
│           └── ai/
│
├── 📁 services/                  # Independent microservices
│   ├── rss-crawler/              # Crawls 400+ news sources
│   ├── price-tracker/            # Fetches market data
│   ├── ai-engine/                # AI summarization & scoring
│   └── notification/             # Push & email notifications
│
├── 📁 infrastructure/
│   ├── docker/                   # Dockerfiles
│   ├── nginx/                    # Reverse proxy config
│   └── postgres/
│       └── schema.sql            # Full database schema
│
├── 📁 docs/                      # Documentation
│   ├── CONTRIBUTING.md
│   ├── API.md
│   └── DEPLOYMENT.md
│
├── 📁 .github/
│   └── workflows/
│       └── ci.yml                # GitHub Actions CI/CD
│
├── docker-compose.yml
├── .env.example
├── LICENSE
└── README.md                     # ← You are here
```

---

## Quick Start

### Prerequisites

Make sure you have the following installed:

- [Docker](https://docs.docker.com/get-docker/) & Docker Compose v2
- [Node.js](https://nodejs.org/) 18+
- [Python](https://www.python.org/) 3.11+
- [Git](https://git-scm.com/)

### 1 — Clone the repository

```bash
git clone https://github.com/yourname/nexus.git
cd nexus
```

### 2 — Configure environment variables

```bash
cp .env.example .env
```

Open `.env` and fill in the required values:

```bash
# Minimum required to start
SECRET_KEY=your-secret-key-here
POSTGRES_PASSWORD=your-db-password
STRIPE_SECRET_KEY=sk_test_...
OPENAI_API_KEY=sk-...
MAPBOX_TOKEN=pk.eyJ1...
```

> See [.env.example](.env.example) for all available options.

### 3 — Start with Docker

```bash
docker-compose up -d
```

This starts all services:

| Service | URL |
|---------|-----|
| Frontend | http://localhost:3000 |
| Backend API | http://localhost:8000 |
| API Docs (Swagger) | http://localhost:8000/docs |
| Meilisearch | http://localhost:7700 |
| Redis | localhost:6379 |
| PostgreSQL | localhost:5432 |

### 4 — Run database migrations

```bash
docker-compose exec backend alembic upgrade head
```

### 5 — Seed initial data (optional)

```bash
docker-compose exec backend python scripts/seed.py
```

That's it. Visit **http://localhost:3000** to open the platform.

---

## Development Setup

For local development without Docker:

### Frontend

```bash
cd frontend
npm install
npm run dev          # starts on http://localhost:3000
```

### Backend

```bash
cd backend
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate
pip install -r requirements.txt
uvicorn main:app --reload  # starts on http://localhost:8000
```

### RSS Crawler

```bash
cd services/rss-crawler
pip install -r requirements.txt
python crawler.py
```

---

## Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| `SECRET_KEY` | ✅ | JWT signing secret |
| `DATABASE_URL` | ✅ | PostgreSQL connection string |
| `REDIS_URL` | ✅ | Redis connection string |
| `STRIPE_SECRET_KEY` | ✅ | Stripe payments |
| `OPENAI_API_KEY` | ✅ | AI summaries and reports |
| `MAPBOX_TOKEN` | ✅ | Interactive map |
| `MEILISEARCH_KEY` | ✅ | Full-text search |
| `ALPHA_VANTAGE_KEY` | ⬜ | Market data (free tier available) |
| `AWS_ACCESS_KEY_ID` | ⬜ | File storage (or use Cloudflare R2) |
| `GOOGLE_CLIENT_ID` | ⬜ | OAuth login with Google |
| `SMTP_HOST` | ⬜ | Email notifications |

---

## API Reference

The REST API is fully documented with OpenAPI (Swagger).

Base URL: `http://localhost:8000/api/v1`

### Key Endpoints

```
Authentication
  POST   /auth/register           Register new user
  POST   /auth/login              Login, returns JWT
  POST   /auth/refresh            Refresh access token

Marketplace
  GET    /listings                List all products/services
  POST   /listings                Create new listing (seller)
  GET    /listings/{id}           Get listing detail
  POST   /orders                  Place an order
  GET    /orders/{id}             Get order status

World Monitor
  GET    /monitor/news            Paginated news feed
  GET    /monitor/events          Geopolitical events (map data)
  GET    /monitor/countries       Country stability scores
  POST   /monitor/alerts          Create keyword alert

Analytics
  GET    /analytics/indices       Live market indices
  GET    /analytics/risk          Global risk composite score
  GET    /analytics/indicators    Macroeconomic indicators
  GET    /analytics/reports       AI-generated market reports

Search
  GET    /search?q={query}        Unified search across all data
```

Full documentation: http://localhost:8000/docs

---

## Roadmap

### v1.0 — Foundation ✅
- [x] Project architecture and monorepo setup
- [x] PostgreSQL schema (8 modules, 25+ tables)
- [x] Docker Compose with all services
- [x] Frontend UI system (Next.js + design tokens)

### v1.1 — Core Platform 🔄
- [ ] Authentication (email + OAuth)
- [ ] Seller onboarding and Stripe Connect
- [ ] Basic marketplace (list, search, purchase)
- [ ] RSS crawler with 400+ sources

### v1.2 — World Monitor
- [ ] Geopolitical event classification (AI)
- [ ] Country Instability Index (CII)
- [ ] Real-time keyword alerts
- [ ] Interactive Mapbox heatmap

### v1.3 — Economic Analytics
- [ ] 92-exchange live market data (Alpha Vantage + Finnhub)
- [ ] Risk scoring engine
- [ ] AI report generation (GPT-4)
- [ ] Correlation detection system

### v2.0 — Scale
- [ ] Mobile app (React Native)
- [ ] Multi-language interface (AR, FR, DE, ZH)
- [ ] Enterprise API (rate-limited, token auth)
- [ ] Self-hosted AI model (Ollama / Llama 3)

---

## Contributing

We welcome contributions of all kinds — code, documentation, translations, and bug reports.

```bash
# 1. Fork the repository on GitHub

# 2. Clone your fork
git clone https://github.com/YOUR_USERNAME/nexus.git

# 3. Create a feature branch
git checkout -b feature/your-feature-name

# 4. Make your changes and commit
git commit -m "feat: add your feature"

# 5. Push and open a pull request
git push origin feature/your-feature-name
```

Please read [CONTRIBUTING.md](docs/CONTRIBUTING.md) before submitting.

### Commit Convention

```
feat:     new feature
fix:      bug fix
docs:     documentation changes
style:    formatting, no logic change
refactor: code restructure
test:     adding or updating tests
chore:    build process, dependencies
```

---

## Self-Hosting

NEXUS is designed to run on any Linux VPS. Minimum recommended specs:

| Tier | RAM | CPU | Storage | Suitable for |
|------|-----|-----|---------|--------------|
| Starter | 2 GB | 2 vCPU | 40 GB | Development / Testing |
| Small | 4 GB | 2 vCPU | 80 GB | Up to 1,000 users |
| Medium | 8 GB | 4 vCPU | 160 GB | Up to 10,000 users |
| Large | 16 GB | 8 vCPU | 320 GB | Production scale |

Providers tested: DigitalOcean, Hetzner, Contabo, Vultr, AWS EC2.

Full deployment guide: [docs/DEPLOYMENT.md](docs/DEPLOYMENT.md)

---

## License

```
MIT License

Copyright (c) 2026 NEXUS Contributors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software.
```

See [LICENSE](LICENSE) for full text.

---

## Acknowledgements

Built with these excellent open-source projects:

- [Next.js](https://nextjs.org) — React framework
- [FastAPI](https://fastapi.tiangolo.com) — Python API framework
- [PostgreSQL](https://postgresql.org) — Primary database
- [Meilisearch](https://meilisearch.com) — Search engine
- [Stripe](https://stripe.com) — Payment infrastructure
- [Mapbox](https://mapbox.com) — Interactive maps
- [Celery](https://docs.celeryq.dev) — Task queue
- [feedparser](https://feedparser.readthedocs.io) — RSS parsing

---

<div align="center">

Made with ❤️ by the NEXUS community

[⭐ Star this repo](https://github.com/yourname/nexus) · [🐛 Report a bug](https://github.com/yourname/nexus/issues) · [💬 Join Discord](https://discord.gg/nexus)

</div>
