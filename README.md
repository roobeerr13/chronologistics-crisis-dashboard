# 🧭 ChronoLogistics Crisis Dashboard

**Real-time command & control system for strategic response to climate crises**

An interactive web dashboard built as a contingency-planning tool. It centralizes risk monitoring, scenario simulation, and emergency protocol activation in a single live interface.

## Overview

The dashboard has three main views:

1. **Precog — Tactical Risk Monitor**
   Heatmap visualization of critical clusters, with an interactive simulator that calculates cascading risk levels in real time.

2. **Chronos — 2040 Strategic Vision**
   Lets the user choose between two future strategies ("Green Fortress" vs "Tech Bunker"), with generated visuals and argumentation for each.

3. **K-Lang — Interactive Battle Manual**
   Simulates operational conditions (wind, rainfall) and automatically activates the matching emergency protocol: *VÍSPERA*, *CÓDIGO ROJO*, or *RENACIMIENTO*.

## Risk Prediction Logic

The `predecir_riesgo()` function calculates cascading risk based on two variables:
- Average wind speed
- Rainfall intensity

Output is classified into three levels: `LOW`, `MODERATE`, `HIGH`.

## Emergency Protocols

Defined in `protocols.json` and triggered by simulated conditions:
- **VÍSPERA** — wind < 50 km/h
- **CÓDIGO ROJO** — wind > 90 km/h
- **RENACIMIENTO** — flooding > 300 cm

Each protocol includes a trigger condition and a list of operational actions.

## Tech Stack

- **Frontend & Backend:** [Streamlit](https://streamlit.io/)
- **Language:** Python 3.9+
- **Visualization:** dynamic metrics, interactive sliders, pre-generated imagery

## Installation

\```bash
git clone https://github.com/roobeerr13/chronologistics-crisis-dashboard.git
cd chronologistics-crisis-dashboard
pip install -r requirements.txt
python -m streamlit run app.py
\```


