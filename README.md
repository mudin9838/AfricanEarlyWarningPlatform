# African Early Warning & Decision Intelligence Platform (AEWDIP)

An AI-powered platform designed to help the African Union monitor emerging risks, analyze crises, and make data-driven decisions across member states.

---

## 🚀 The Core Problem
The AU receives information from many sources, but decision-makers need a unified, intelligent system to:
* Monitor continental risks (Food security, disease outbreaks, and climate disasters).
* Detect emerging crises early instead of just reporting them late.
* Provide actionable response recommendations to leaders.

---

## 🏛️ Multi-Level Users
* **AU Headquarters:** Views the continental dashboard, tracks high-level risks, and generates executive reports.
* **Regional Communities (e.g., IGAD, ECOWAS):** Monitors regional trends and coordinates cross-border responses.
* **Country Officers:** Submits local incidents and manages national data dashboards.

---

## 🛠️ Core Modules (MVP)

1. **Incident Management:** Allows country officers to report localized events (e.g., flooding, droughts, or public health spikes).
2. **AI Analysis Engine:** Automatically reads incoming text reports to generate short summaries, classify risk types, and tag severity levels using Language Models.
3. **Risk Scoring Engine:** Calculates threat levels using a clean mathematical formula based on incident frequency, impact radius, and geographic spread.
4. **Continental Map Dashboard:** An interactive Africa map (built with Blazor and Leaflet) showing visual risk hotspots (Green, Yellow, Orange, Red) with click-to-drill-down capabilities.
5. **Alert System:** Dispatches automated email or webhook alerts the moment an incident crosses into a critical risk tier.

---

## 🏗️ Tech Stack
* **Backend:** ASP.NET Core 9 Web API (Clean Architecture / CQRS with MediatR)
* **Frontend:** Razor Web App (Interactive Server Mode)
* **Database:** PostgreSQL + PostGIS (for spatial and map data)
* **Background Jobs:** Hangfire (for processing AI calls and alerts)
* **AI Integration:** Semantic Kernel (supporting Azure OpenAI or local models via Ollama)
* **Deployment:** Docker & Azure

---

## 📂 Project Structure
```text
📁 src
 ├── 📁 AEWDIP.Domain           # Core entities and business logic
 ├── 📁 AEWDIP.Application      # CQRS commands, queries, and interfaces
 ├── 📁 AEWDIP.Infrastructure   # Databases, AI services, and background jobs
 ├── 📁 AEWDIP.HttpApi          # REST API endpoints
 └── 📁 AEWDIP.BlazorWeb        # Interactive map and user dashboard UI
