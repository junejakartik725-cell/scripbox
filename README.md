# Scripbox Robo-Advisory AI Model

## AI in Digital Wealth Management — Scripbox Robo-Advisory Case Study

An end-to-end **AI/ML demonstration for digital wealth management**, modeled around a Scripbox-style robo-advisory workflow. The project combines customer risk profiling, mutual-fund ranking, personalized fund shortlisting, and SIP wealth projection.

> **Academic project:** The dataset used by the model is synthetic and is intended for demonstration and learning. It is not a production investment-advisory system.

## 🎯 Project Objective

The project demonstrates how an AI-driven wealth platform can transform:

**Client Data → Data Cleaning → Feature Engineering → Risk Prediction → Fund Ranking → Personalized Shortlist → SIP Projection**

The business problem addressed is the difficulty of manually profiling large numbers of investors and comparing a large mutual-fund universe consistently.

## 🤖 ML / AI Approach

### 1. Risk Profiling — Random Forest Classifier

A **Random Forest Classifier** predicts one of three investor risk categories:

* Conservative
* Moderate
* Aggressive

The model uses onboarding and behavioral indicators such as:

* Age
* Monthly income
* Dependents
* Investment horizon
* Monthly investable surplus
* Existing investments
* Reaction to a market drop

### 2. Explainable AI — Feature Importance

The model exposes **Gini feature importance** to show which inputs contribute most to the risk-profiling model.

This supports the project's focus on explainability and responsible AI in financial applications.

### 3. Mutual Fund Ranking — Multi-Factor Scoring

The recommendation engine creates a synthetic fund catalogue and calculates a composite score using:

| Factor        | Weight |
| ------------- | -----: |
| 3-year return |    30% |
| 5-year return |    20% |
| Sharpe ratio  |    25% |
| Expense ratio |    15% |
| Volatility    |    10% |

Returns and Sharpe ratio are treated as higher-is-better factors, while expense ratio and volatility are treated as lower-is-better factors.

### 4. Personalized Fund Shortlisting

The predicted risk category is mapped to suitable fund universes:

* **Conservative:** Liquid Debt, Corporate Bond
* **Moderate:** Hybrid Allocator, Large Cap Equity, Corporate Bond
* **Aggressive:** Small Cap Equity, Mid Cap Equity, Large Cap Equity

The system then selects highly ranked funds from the relevant categories.

### 5. SIP Wealth Projection

The project includes a SIP future-value engine that demonstrates how different assumed annual growth rates could affect long-term wealth projections.

**Important:** These are model assumptions/projections for an academic demonstration, not guaranteed investment returns.

## 📊 Dataset

The notebook generates **2,000 synthetic customer records**.

It intentionally introduces data-quality issues such as:

* Missing values
* Extreme investment-value outliers
* Noisy risk-score generation

The preprocessing stage uses **median imputation** and **RobustScaler**.

The fund-ranking section generates a synthetic catalogue of **80 funds** across multiple asset classes.

No real customer data is included.

## 🧠 Feature Engineering

The project derives additional business-oriented features:

* `surplus_to_income_ratio`
* `asset_leverage_ratio`
* `age_horizon_interaction`

Feature selection then applies:

1. Variance filtering
2. Correlation-based multicollinearity filtering

## 🛠️ Tech Stack

* Python
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

## 📁 Repository Structure

```text
Scripbox-Robo-Advisory-AI-Model/
│
├── Scripbox_Robo_Advisory_AI_Model_v2-2.ipynb
├── Scripbox_AI_Case_Study-2.pptx
└── README.md
```

## ▶️ How to Run

1. Install Python 3.x.
2. Install the required libraries:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```

3. Open the notebook:

```bash
jupyter notebook
```

4. Run the notebook cells from top to bottom.

The random seed is fixed at **42** to make the synthetic-data workflow reproducible.

## 🔄 ML Pipeline

```text
Synthetic Customer Data
        ↓
Data Cleaning
        ↓
Robust Scaling
        ↓
Feature Engineering
        ↓
Feature Selection
        ↓
Random Forest Risk Classifier
        ↓
XAI Feature Importance
        ↓
Multi-Factor Fund Scoring
        ↓
Risk-Based Fund Shortlist
        ↓
SIP Wealth Projection
```

## ⚠️ Disclaimer

This repository is an **academic AI/ML case study**. The customer and mutual-fund datasets are synthetic. The model, fund scores, risk classifications, and wealth projections should **not** be treated as financial advice or as a substitute for a SEBI-registered investment adviser.

## 👨‍🎓 Project

**Student:** Kartik juneja 
**Institution:** Chitkara Business School
**Course:** AI & ML
**Project:** AI in Digital Wealth Management — Scripbox Robo-Advisory Case Study
**Year:** 2026

## 📌 Suggested GitHub Description

**End-to-end AI/ML robo-advisory case study modeled on Scripbox, featuring Random Forest risk profiling, XAI feature importance, multi-factor mutual-fund ranking, personalized fund shortlisting, and SIP wealth projection using synthetic data.**
\
