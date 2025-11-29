# EROS-Datathon
Datathon Sheridan
# 🚨 Emergency Response Optimization System (EROS)

AI-powered backend and web dashboard to manage and optimally stage emergency response vehicles (Ambulances, Firetrucks, Police) using predictive data and the Gemini API.

---

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Architecture](#architecture)
- [Prerequisites](#prerequisites)
- [Quick Start](#quick-start)
- [Usage](#usage)
- [Configuration](#configuration)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

---

## Overview
EROS visualizes vehicle positions on a map, persists data in SQLite, and uses predictive and AI-driven allocation to suggest optimal staging and dispatch decisions.

## Features
- Real-time map dashboard (Google Maps Platform)
- Persistent storage with SQLite
- Predictive repositioning using environmental and historical data
- AI-driven allocation via Gemini API (optimize_allocation_ai.py)
- Simple dispatch endpoint for incident simulation and unit dispatch

## Architecture
- Backend: Python (Flask/FastAPI or similar)
- Storage: SQLite
- Frontend: Web dashboard (Google Maps)
- AI: Gemini API for complex allocation suggestions

## Prerequisites
- Python 3.8+
- API keys:
  - Google Maps API Key (map visualization)
  - Gemini API Key (AI optimization)

## Quick Start

1. Create and activate a virtual environment
- Windows (PowerShell / CMD)
```powershell
# Create venv
python -m venv venv
# Activate (PowerShell)
.\venv\Scripts\Activate.ps1
# Activate (CMD)
.\venv\Scripts\activate.bat
```
- macOS / Linux
```bash
python3 -m venv venv
source venv/bin/activate
```

2. Install dependencies
```bash
pip install -r requirements.txt
```

3. Configure environment variables (recommended)
- Windows (PowerShell)
```powershell
$env:GOOGLE_MAPS_API_KEY = "your_google_maps_key"
$env:GEMINI_API_KEY = "your_gemini_api_key"
```
- macOS / Linux
```bash
export GOOGLE_MAPS_API_KEY="your_google_maps_key"
export GEMINI_API_KEY="your_gemini_api_key"
```

4. Run the application (example)
```bash
# adjust to your project's run command (Flask, FastAPI uvicorn, or a script)
python run_server.py
```

## Usage
- Open the dashboard HTML in a browser to view vehicle positions (requires Google Maps API key).
- Use the provided API endpoints to:
  - Simulate incidents and dispatch nearest available unit
  - Trigger AI optimization (optimize_allocation_ai.py) to get staging suggestions

## Configuration
- Database: SQLite file (default path in project). Adjust in config if needed.
- AI: Set GEMINI_API_KEY to enable AI-driven allocation. See optimize_allocation_ai.py for request/parameter details.

## Project Structure (top-level)
- main/README.md (this file)
- app/ or src/ — backend service
- dashboard/ — frontend map visualization
- data/ — SQLite DB, migrations
- scripts/optimize_allocation_ai.py — Gemini integration
- requirements.txt

## Contributing
- Fork, create a feature branch, add tests, and open a PR.
- Keep changes focused and document config/behavior changes.


