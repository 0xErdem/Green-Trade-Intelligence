# 🌍 Green-Trade Intelligence: AI-Driven CBAM & ETS Financial Simulator

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-orange.svg)
![XGBoost](https://img.shields.io/badge/XGBoost-Time%20Series-green.svg)
![FastAPI](https://img.shields.io/badge/FastAPI-Microservice-teal.svg)
![Sustainability](https://img.shields.io/badge/Domain-Sustainability%20&%20EU%20Green%20Deal-brightgreen.svg)

## 📌 Executive Summary
This project bridges the gap between **Environmental Compliance** and **Corporate Finance**. With the EU's Carbon Border Adjustment Mechanism (CBAM) taking full financial effect, industrial manufacturers face unprecedented operational costs. 

This repository provides an end-to-end, data-driven simulation architecture that translates complex supply chain emission data into actionable financial hedging strategies. It goes beyond simple carbon footprint calculation by utilizing **Machine Learning (Isolation Forest & XGBoost)** to detect supply chain inefficiencies and forecast ETS (Emissions Trading System) price volatility.

## 🚀 Business Value & Strategic Insights
Designed with a "Business Development & Sustainability" mindset, this simulator delivers three core strategic outputs:
1. **Financial Hedging & Carbon Arbitrage:** Forecasts EU ETS price fluctuations to recommend optimized carbon credit purchasing windows (Buy/Delay/Hold).
2. **Supply Chain De-risking:** Uses automated Anomaly Detection to identify Tier-1 and Tier-2 suppliers with severe energy inefficiencies, enabling targeted procurement interventions.
3. **Multi-Tier BOM (Bill of Materials) Costing:** Calculates embedded Scope 1, 2, and 3 emissions through complex product hierarchies, deducing origin-country carbon taxes from the final CBAM liability.

## 🧠 System Architecture & Methodology

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/f701b0f0-bddd-4dfa-bc75-bd6c11f58728" />


1. **Data Ingestion & Simulation:** Simulates an enterprise-grade ERP extract featuring various material groups, origin countries, and dynamic emission factors.
2. **Anomaly Detection Engine:** Applies `IsolationForest` to flag abnormal carbon intensity clusters within the procurement data, representing either data quality issues or factory-level inefficiencies.
3. **Predictive Financial Modeling:** Integrates live global carbon ETF market data using `yfinance`. Trains an `XGBoost` regressor on time-series features (lags, rolling averages) to forecast near-term carbon price trends.
4. **Cloud-Ready API Deployment:** Encapsulates the core calculation engine within a `FastAPI` endpoint, making the model instantly integrable with existing Corporate Dashboards or SAP systems.

## 🛠️ Tech Stack
* **Data Processing:** `pandas`, `numpy`
* **Machine Learning:** `scikit-learn` (Isolation Forest), `xgboost` (Time-Series Forecasting)
* **Market Data & APIs:** `yfinance` (Live Carbon ETF Data), `FastAPI` (Microservice Deployment)
* **Data Visualization:** `matplotlib`, `seaborn`

## ⚙️ How to Run

```bash
# 1. Clone the repository
git clone [https://github.com/yourusername/green-trade-intelligence.git](https://github.com/yourusername/green-trade-intelligence.git)

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the ML pipeline & generate dashboards
python src/main_pipeline.py

# 4. Start the FastAPI microservice
uvicorn src.api:app --reload
