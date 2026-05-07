# Financial-econometrics-Project3
Regime change detection model applied to Apple Inc. (AAPL) stock returns using a two-state Markov Switching Model to identify structural breaks from 2018 to 2025

---
# Financial Econometrics - Project 3
## Regime Change Detection: Apple Inc. (AAPL) 2018–2025

---

## Overview
This project applies a two-state Markov Switching Model to 
Apple Inc. (AAPL) daily stock returns from January 2018 to 
December 2025. The model detects structural breaks in Apple's 
return-generating process - identifying distinct calm and 
crisis market regimes - and provides detailed parameter 
interpretation, diagnostic analysis, and a practical 
deployment framework for professional investment management.

---

## Dataset
| Attribute | Detail |
|---|---|
| **Asset** | Apple Inc. (AAPL) |
| **Source** | Yahoo Finance via yfinance API |
| **Period** | January 2018 – December 2025 |
| **Frequency** | Daily closing prices |
| **Units** | US Dollars (USD) |
| **Observations** | ~2,009 trading days |

---

## Model
**Markov Switching Model (Hamilton, 1989)**

The model assumes Apple's daily log returns are drawn 
from two distinct distributions depending on the 
prevailing market regime:

- **Regime 0 - Calm/Bull Market:** Low volatility, 
  positive expected returns, high persistence
- **Regime 1 - Crisis/Bear Market:** High volatility, 
  negative expected returns, triggered by events 
  such as COVID-19 (March 2020) and the Federal 
  Reserve rate hike cycle (2022)

Parameters estimated by Maximum Likelihood Estimation:
- Regime-specific means (μ₀, μ₁)
- Regime-specific variances (σ₀², σ₁²)  
- Transition probabilities (p₀₀, p₁₁)

---

## Notebook Structure
The notebook follows the assignment's required 8-section 
structure:

| Section | Content |
|---|---|
| **Definition** | Markov Switching Model equations |
| **Description** | Plain English explanation |
| **Demonstration** | Model fitting + full parameter interpretation |
| **Diagram** | 4 exploratory charts including regime-shaded price chart |
| **Diagnosis** | Residual analysis, Q-Q plot, ACF, AIC/BIC comparison |
| **Damage** | Model limitations + connection to Project 1 challenges |
| **Directions** | Data manipulation recommendations |
| **Deployment** | 5 detailed real-world applications |

---

## Repository Structure
financial-econometrics-project3/
│

├── Financial_Econometrics_Project3.ipynb   # Main notebook

└── README.md                               # This file
