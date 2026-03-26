# 🌦️ Probabilistic Drought Forecasting using Time Series Modeling

> **Predicting long-term drought risk through advanced statistical modeling, Monte Carlo simulation, and anomaly detection on 40+ years of climate data.**

---

## 📌 Overview

This project applies a suite of time series and machine learning techniques to model and forecast drought conditions across multiple regions. Using **Water Balance (WB)** and **SPEI-12** drought indices derived from decades of climate records, the study quantifies drought probability, duration, and severity over a 20-year horizon while rigorously characterizing uncertainty.

---

## 🛠️ Tech Stack

| Category | Tools & Libraries |
|---|---|
| **Language** | Python |
| **Statistical Modeling** | Statsmodels (SARIMA, State Space) |
| **Machine Learning** | Scikit-learn, XGBoost |
| **Simulation** | NumPy (Monte Carlo) |
| **Trend Analysis** | pymannkendall, SciPy |
| **Anomaly Detection** | Scikit-learn (Isolation Forest) |
| **Data & Visualization** | Pandas, Matplotlib, Seaborn |

---

## 🔍 Key Features & Methodology

### 📊 1. Multi-Decadal Climate Data Analysis
- Analyzed **40+ years of climate data** to model long-term drought risk.
- Computed **Water Balance (WB)** and **SPEI-12** drought indices across multiple geographic regions.
- Processed both **daily and monthly** resolution data for comprehensive temporal coverage.

### 🤖 2. Predictive Modeling & Comparison
- Developed and rigorously compared three forecasting approaches:
  - **XGBoost** — gradient-boosted regression for non-linear patterns
  - **SARIMA** — seasonal autoregressive integrated moving average
  - **Structural State Space Models** — for latent-component decomposition
- Evaluated all models using **R²** and **RMSE** metrics on held-out test sets.

### 📈 3. Local Linear Trend (State Space) Modeling
- Implemented **Local Linear Trend** state space models with:
  - Seasonal components to capture annual drought cycles
  - Autoregressive components for short-term dependencies
- Designed to handle **non-stationary climate dynamics** inherent in long climate records.

### 🎲 4. Monte Carlo Probabilistic Projections
- Designed a **Monte Carlo simulation framework** with **1,000+ runs** to generate probabilistic 20-year drought projections.
- Output includes full **uncertainty intervals** (confidence bands) around median forecasts, enabling risk-aware decision-making.

### 📉 5. Trend Detection & Significance Testing
- Applied **Mann-Kendall trend analysis** to detect monotonic trends in drought indices.
- Estimated trend magnitude using **Sen's Slope estimator**.
- Validated statistical significance across all regions and time windows.

### 🚨 6. Anomaly Detection Pipeline
- Built an anomaly detection pipeline combining:
  - **Isolation Forest** for unsupervised outlier identification
  - **Residual analysis** from time series models
- Identified **extreme climate events** and flagged anomalous drought episodes.

### 📐 7. Probabilistic Drought Metrics
- Derived a comprehensive set of probabilistic drought metrics:
  - **Severe drought likelihood** (probability of SPEI ≤ −1.5)
  - **Extreme drought likelihood** (probability of SPEI ≤ −2.0)
  - **Expected drought duration** under projected climate trajectories
  - **Confidence intervals** for all key forecast statistics

---

## 📌 Key Findings

> 📢 The analysis concluded an **absence of a strong deterministic drying trend** in the study regions. The dominant driver of drought variability is **stochastic climate variability** rather than a systematic long-term drying signal — a finding consistent with the behavior of **semi-arid climate systems**.

---

## 📁 Repository Structure

```
📦 Probabilistic-Drought-Forecasting-using-Time-Series-Modeling
 ┣ 📓 Project_1.ipynb    # Main analysis notebook
 ┗ 📄 README.md
```

---

## 🚀 Getting Started

### Prerequisites
```bash
pip install numpy pandas matplotlib seaborn statsmodels scikit-learn xgboost pymannkendall
```

### Run the Notebook
```bash
jupyter notebook Project_1.ipynb
```

---

## 📜 License

This project is open-source and available under the [MIT License](LICENSE).
