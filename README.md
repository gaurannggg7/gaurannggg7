<!-- ====================== HEADER ====================== -->
<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0f766e,50:10b981,100:14b8a6&height=220&section=header&text=Gaurang%20Mohan&fontSize=64&fontColor=ffffff&fontAlignY=38&desc=Software%20Engineer%20%E2%80%A2%20Backend%20Systems%20%E2%80%A2%20Applied%20AI&descSize=20&descAlignY=60" alt="Gaurang Mohan — Software Engineer, Backend Systems and Applied AI" />

### Software Engineer · Backend & Full-Stack · Applied AI

I build software around real workflows: live data, reliable APIs, and AI outputs people can inspect.

<p>
  <code>Python</code> · <code>TypeScript</code> · <code>FastAPI</code> · <code>React / Next.js</code> · <code>PostgreSQL</code> · <code>LangGraph</code>
</p>

<a href="https://gaurangmohan.vercel.app/"><img src="https://img.shields.io/badge/Portfolio-0F766E?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio" /></a>
<a href="mailto:gaurangmohan25@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
<a href="https://linkedin.com/in/gaurang-mohan"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
<a href="https://huggingface.co/gaurannggg7"><img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" alt="Hugging Face" /></a>

[About](#about) · [Featured Projects](#featured-projects) · [Toolbox](#toolbox) · [Experience](#experience) · [Education](#education) · [Connect](#connect)

</div>

---

## About

I'm a Computer Science graduate from **Arizona State University**, focused on **backend engineering, full-stack products, and applied AI**.

- **Real-time systems:** MarketOps combines streaming market-data simulation, incident workflows, and an auditable PostgreSQL backend.
- **Applied AI:** Baseline separates financial calculations in Python from model-generated analysis; Bellwether tests whether prompt changes introduce regressions.
- **Latest build:** Forge is my private personal dashboard for job applications, habits, journaling, and progression.
- **Open to:** Software Engineer, Backend, Full-Stack, and Applied AI roles. Open to relocating across the U.S.

<div align="center">
<img src="https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExdzg0a3dvenVtdWQ2NzJpZXpqcGs2cmJyejN4ZHVmeGZ1Ymhmcmw3dSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/rNK2rnzqXupoIgl2BA/giphy.gif" width="240" alt="Zoro animation" />
</div>

---

## Featured Projects

### MarketOps — Real-Time Market Monitoring & Incident Management

**[Code](https://github.com/gaurannggg7/MarketOps) · [Demo](https://market-ops.vercel.app) · [Architecture](https://github.com/gaurannggg7/MarketOps/blob/main/docs/architecture.md) · [Benchmarks](https://github.com/gaurannggg7/MarketOps/blob/main/docs/performance.md)**

A market-operations workspace to monitor quote freshness and spreads, investigate automatic incidents, and work through acknowledgment, recovery, and resolution with a full audit trail.

- **Streaming UI:** AG Grid and D3 charts over ordered WebSocket snapshots and deltas, with 200 synthetic instruments.
- **Backend integrity:** session authentication, CSRF protection, role-based access, database-backed incident integrity, and versioned rule updates.
- **Measured locally:** 50 quotes/second across five WebSocket clients for 10 minutes with **zero sequence gaps**.
- **Verification:** pytest, Vitest/React Testing Library, Playwright workflows, API contract checks, and GitHub Actions.

**Stack:** React · TypeScript · AG Grid · D3 · FastAPI · PostgreSQL · WebSockets · Docker

*Synthetic data only. Benchmarks are local measurements; the public demo runs on free hosting and may take 1–2 minutes to wake.*

### Baseline — Financial Intelligence with Deterministic Calculations

**[Code](https://github.com/gaurannggg7/cpg-cfo-agent) · [Demo](https://cpg-cfo-agent.vercel.app) · [Architecture](https://github.com/gaurannggg7/cpg-cfo-agent/blob/main/ARCHITECTURE.md) · [Evaluation](https://github.com/gaurannggg7/cpg-cfo-agent/blob/main/eval/RESULTS.md)**

Turns transaction CSVs into a financial brief using a LangGraph workflow: **three LLM calls plus a deterministic Python runway node**.

- Computes category totals in pandas and runway in Python, while models handle categorization, anomaly screening, and narrative summaries.
- Validates CSV input before model calls and maps malformed files and upstream failures to structured API errors.
- Provides guest access, Firebase authentication, per-user saved analysis history, and an MCP integration.
- **Earlier-model evaluation:** eliminated 10 unhandled server errors; **27/27 evaluated adversarial cases passed**, with two additional cases not run because of provider quota. Full-corpus model results have not been re-measured on the current model.

**Stack:** Next.js · TypeScript · FastAPI · LangGraph · Groq · pandas · Firebase · FastMCP

### Bellwether — AI Evaluation & Regression Gates

**[Code & Methodology](https://github.com/gaurannggg7/AI-Evaluation-Observability-Framework-for-Clinical-AI-Companions)**

An independent evaluation prototype for comparing AI response versions using **60 synthetic scenarios, seven evaluation dimensions, and three hard gates**.

- Separates generation from evaluation and keeps reference labels out of generator, classifier, and evaluator inputs.
- Records auditable routing decisions, evaluator disagreements, and per-scenario traces in SQLite.
- **Reproducible mock-mode result:** blocked a candidate when hard-gate failures rose from **8/60 to 16/60**, even though urgent-routing recall stayed unchanged.
- Exposes regression comparisons, failures, and observability through a Streamlit dashboard; blocking regressions return a nonzero CLI exit code.

**Stack:** Python · pytest · SQLite · Streamlit · Evaluation Pipelines

*Entirely synthetic, deterministic mock-mode results. Independent engineering prototype; not clinically validated.*

### Agentic OSINT Analyst — Retrieval-Grounded Research

**[Code](https://github.com/gaurannggg7/osint-synthesis-engine) · [Retrieval Evaluation](https://github.com/gaurannggg7/osint-synthesis-engine/blob/main/eval/STAGE_5_RESULTS.md)**

A two-node LangGraph workflow that retrieves public-record excerpts and synthesizes a report with numbered citations readers can inspect.

- Normalizes records from OFAC, SEC EDGAR, and CourtListener into a searchable corpus.
- Compares vector, BM25, and reciprocal-rank-fusion retrieval on a **17-query evaluation set**.
- Returns source excerpts alongside reports, with input validation, rate limiting, and explicitly labeled prerecorded demo responses.

**Stack:** Python · FastAPI · LangGraph · Chroma · MiniLM · Next.js

*Working prototype. Citation links support inspection; they do not automatically verify that every claim is grounded.*

### SignLink — Speech/Text to ASL Video

**[Code](https://github.com/gaurannggg7/signlink) · [Hugging Face Demo](https://huggingface.co/spaces/gaurannggg7/Signlink)**

An accessibility-focused pipeline that transcribes speech, produces ASL gloss, resolves tokens to a **1,566-asset motion-capture library**, and stitches clips into playable video.

- Uses exact/phrase matching, suffix-based fallback, and fingerspelling for unknown words.
- Separates transcription, gloss generation, asset retrieval, and FFmpeg rendering for CPU-hosted deployment.

**Stack:** Python · Whisper · Hugging Face · FFmpeg · Streamlit · Docker

### Forge — Personal Workflow Dashboard

A private full-stack app I use to track job applications, daily habits, journal entries, and RPG-style progression in one place.

- Application statuses, follow-up flags, habit check-ins, and daily/weekly quests tied to logged activity.
- Next.js route handlers backed by Neon PostgreSQL, with optional proof-image uploads.

**Stack:** Next.js · TypeScript · Tailwind CSS · PostgreSQL · Recharts · Vercel

*Private repository.*

---

## Toolbox

| Area | Technologies |
|---|---|
| **Languages** | Python, TypeScript, JavaScript, SQL, Java, C++ |
| **Backend & Data** | FastAPI, PostgreSQL, SQLAlchemy, REST APIs, WebSockets, Firebase |
| **Frontend** | React, Next.js, AG Grid, D3, Tailwind CSS |
| **Applied AI** | LangGraph, FastMCP, Groq, Chroma, pandas, scikit-learn, PyTorch, Hugging Face |
| **Cloud & Delivery** | AWS, Docker, Terraform, Vercel, GitHub Actions, Linux |
| **Testing** | pytest, Vitest, React Testing Library, Playwright |

---

## Experience

**Visionary Hands (ASU EPICS)** — *Project Team Lead & Embedded ML Engineer*  
Jan 2024 – Dec 2025

- Led development of a wearable ASL-translation glove, improving gesture-classification accuracy from **65% to 95%**, with **60 FPS** processing and measured **sub-50 ms** latency.
- Received a **$1,000 EPICS Elite Pitch award**.

---

## Education

**Arizona State University** — Ira A. Fulton Schools of Engineering  
**B.S. Computer Science** · Minor in Data Science · May 2026  
Cum Laude · **3.40/4.0 GPA** · New American University Scholar

---

## Connect

- **Portfolio:** [gaurangmohan.vercel.app](https://gaurangmohan.vercel.app/)
- **Email:** [gaurangmohan25@gmail.com](mailto:gaurangmohan25@gmail.com)
- **LinkedIn:** [linkedin.com/in/gaurang-mohan](https://linkedin.com/in/gaurang-mohan)
- **Hugging Face:** [huggingface.co/gaurannggg7](https://huggingface.co/gaurannggg7)

<div align="center">

<img src="assets/ronaldo.gif" width="240" alt="Cristiano Ronaldo animation" />

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:14b8a6,50:10b981,100:0f766e&height=120&section=footer" alt="Teal wave footer" />

</div>
