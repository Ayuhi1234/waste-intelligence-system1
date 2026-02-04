# ♻️ Waste Intelligence System

![Status](https://img.shields.io/badge/Status-MVP%20Complete-success)
![Stack](https://img.shields.io/badge/Tech-Node.js%20%7C%20TypeScript%20%7C%20PostgreSQL-blue)
![Role](https://img.shields.io/badge/Focus-Founding%20Engineer-purple)

**A scalable, modular monolith designed to ingest, validate, and analyze IoT waste telemetry data.**

---

## 📖 Project Overview
This repository represents a "Vertical Slice" of the Waste Intelligence System. It demonstrates a pragmatic approach to building IoT infrastructure, prioritizing **development velocity** and **type safety** over premature optimization.

### 🎯 Key Objectives
1.  **Ingest** high-volume telemetry (Fill Levels, Battery, Location) via HTTP/MQTT.
2.  **Validate** data strictly at the edge using **Zod** to protect the database.
3.  **Analyze** trends asynchronously using a decoupled Python ML service.
4.  **Visualize** operations via a React Dashboard (planned).

---

## 🏗️ Repository Structure
This project is organized to separate concerns while keeping the codebase "Intern-Friendly."

| Folder | Description |
| :--- | :--- |
| **`/backend-api`** | **(Part B)** The Core Node.js + TypeScript API. Contains `app.ts`, `routes.ts`, and Zod schemas. |
| **`/docs`** | **(Part A)** Architecture Diagrams, Trade-off Decisions, and System Design logic. |
| **`/intern-plan`** | **(Part C)** 5-Day Sprint Plan, Onboarding Guide, and Sample Code Reviews. |
| **`real-world-thinking.md`** | **(Part D)** Strategic Q&A regarding timeline cuts and avoiding over-engineering. |

---

## ⚡ Quick Start (Backend)
I designed the backend to be "Clone & Run" to minimize onboarding friction for new interns.

### Prerequisites
* Node.js v18+
* npm

### Installation
```bash
# 1. Navigate to the backend service
cd backend-api

# 2. Install dependencies
npm install

# 3. Start the development server
npm run dev

👉 **[View the Detailed Sprint Plan](intern-plan/sprint-plan.md)**
👉 **[View Sample Code Review](intern-plan/code-review-example.md)**
