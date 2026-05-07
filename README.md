# Financial-econometrics-Project3
Regime change detection model applied to Apple Inc. (AAPL) stock returns using a two-state Markov Switching Model to identify structural breaks from 2018 to 2025

---
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

---

## Key Findings
1. Two statistically distinct regimes confirmed in 
   Apple's return history - calm and crisis states 
   differ by approximately 3x in annualised volatility
2. The COVID-19 crash of March 2020 is identified as 
   the most prominent regime transition in the sample
3. The 2-regime model outperforms a single constant 
   distribution baseline on both AIC and BIC criteria
4. Crisis regimes are highly persistent once initiated - 
   lasting several weeks on average before reverting

---

## How to Run
1. Open `Financial_Econometrics_Project3.ipynb` in 
   Google Colab or Jupyter Notebook
2. Run **Runtime → Run All**
3. All data is downloaded automatically via the 
   yfinance API - no manual data download required

---

## References
- Hamilton, James D. "A New Approach to the Economic 
  Analysis of Nonstationary Time Series and the Business 
  Cycle." *Econometrica*, vol. 57, no. 2, 1989, 
  pp. 357–384.
- Hull, John C. *Options, Futures, and Other Derivatives*. 
  10th ed., Pearson, 2018.
- Tsay, Ruey S. *Analysis of Financial Time Series*. 
  3rd ed., Wiley, 2010.
- Yahoo Finance. "Apple Inc. (AAPL) Historical Data." 
  *Yahoo Finance*, 2025.

---

## Course Information
**Course:** Financial Econometrics / Applied Time Series  
**Project:** Project 3 - Regime Change Detection  
**Submitted to:** chitzlee@gmail.com
