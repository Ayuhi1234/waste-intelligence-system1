<div align="center">

  # ♻️ Waste Intelligence System
  ### IoT Telemetry Ingestion & Analysis Engine

  <p>
    <img src="https://img.shields.io/badge/Role-Founding%20Engineer-7209b7?style=for-the-badge" alt="Role" />
    <img src="https://img.shields.io/badge/Stack-Node.js%20%7C%20TypeScript%20%7C%20Postgres-blue?style=for-the-badge" alt="Stack" />
    <img src="https://img.shields.io/badge/Status-MVP%20Ready-success?style=for-the-badge" alt="Status" />
    <img src="https://img.shields.io/badge/Validation-Zod%20Strict-orange?style=for-the-badge" alt="Validation" />
  </p>

  <p>
    <b>A scalable, modular monolith designed to ingest, validate, and analyze IoT waste telemetry data.</b>
    <br />
    <i>Pragmatic. Type-Safe. Built for Velocity.</i>
  </p>

</div>

---

## 🧐 Project Overview

This repository represents a **"Vertical Slice"** of the Waste Intelligence System. It demonstrates a **Founding Engineer's approach** to building IoT infrastructure: prioritizing development velocity and type safety over premature optimization.

### 🎯 Key Objectives
| Feature | Description |
| :--- | :--- |
| 📡 **Ingestion** | Handle high-volume telemetry (Fill Levels, Battery) via HTTP/MQTT. |
| 🛡️ **Safety** | Strict edge validation using **Zod** to protect the database integrity. |
| 🧠 **Intelligence** | Asynchronous trend analysis using a decoupled **Python ML service**. |
| 🚀 **Velocity** | A "Clone & Run" environment designed for rapid intern onboarding. |

---

## 📂 Repository Structure

I organized this project to separate concerns while keeping the codebase flat and "Intern-Friendly."

| Folder | Content & Purpose |
| :--- | :--- |
| **[`/backend-api`](./backend-api)** | **(Part B)** The Core Node.js + TypeScript API. Contains `app.ts`, `routes.ts`, and Zod schemas. |
| **[`/docs`](./docs)** | **(Part A)** Architecture Diagrams, Trade-off Decisions, and System Design logic. |
| **[`/intern-plan`](./intern-plan)** | **(Part C)** 5-Day Sprint Plan, Onboarding Guide, and Sample Code Reviews. |
| **`real-world-thinking.md`** | **(Part D)** Strategic Q&A regarding timeline cuts and avoiding over-engineering. |

---

## ⚡ Quick Start (Backend)

*Prerequisites: Node.js v18+, npm*

```bash
# 1. Navigate to the backend service
cd backend-api

# 2. Install dependencies
npm install

# 3. Start the development server
npm run dev

👉 **[View the Detailed Sprint Plan](intern-plan/sprint-plan.md)**
👉 **[View Sample Code Review](intern-plan/code-review-example.md)**

✅ Success: The API will listen on http://localhost:3000. Test it via GET /health.

🧠 Technical Strategy (The "Why")
<details> <summary><b>1. Architecture: The Modular Monolith</b> (Click to expand)</summary>


Decision: I chose a Modular Monolith over Microservices.

Reasoning: At this stage (0-10k sensors), network latency and DevOps complexity are the enemies. A monolith allows us to share types, debug easily, and ship the MVP in days, not weeks.

👉 See full details in docs/architecture_decisions.md

</details>

<details> <summary><b>2. Database: PostgreSQL with JSONB</b> (Click to expand)</summary>


Decision: Single PostgreSQL instance using JSONB for sensor logs.

Reasoning: We don't need the complexity of managing a separate Time-Series DB (InfluxDB) yet. Postgres handles JSONB efficiently enough for our current scale.

</details>

<details> <summary><b>3. Safety: TypeScript + Zod</b> (Click to expand)</summary>


Decision: Strict Mode enabled; Runtime validation on all inputs.

Reasoning: This acts as a safety net for junior engineers, preventing "undefined" errors from crashing production.

</details>

👥 Intern Management & Onboarding
As a Founding Engineer, my role includes mentorship. I have prepared a structured Week 1 Sprint to get interns shipping value immediately.

🎨 Frontend Goal: Ship a "Hello World" Dashboard using Component Libraries (Day 1-5).

🤖 ML Goal: Move from Mock Data → Logistic Regression Model (Day 1-5).

📝 Code Review: Focus on architectural patterns (e.g., Fixing N+1 Queries) rather than syntax nitpicking.

👉 View the Detailed Sprint Plan

🔮 Future Roadmap
✅ Phase 1 (Now): Solid Monolith, Single DB, REST API.

🚧 Phase 2 (>10k Sensors): Introduce InfluxDB for time-series data; move Ingestion to Go/Rust.

🔮 Phase 3 (>1M Sensors): Split into Microservices (Ingestion vs. Analytics vs. User Mgmt).

<div align="center">

Submitted by Ayushi


Founding Engineer Candidate

</div>
