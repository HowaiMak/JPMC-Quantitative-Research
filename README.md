# JPMC Quantitative Research Job Simulation Programme

Conducted via **Forage** between **July 2024** to **August 2024**.

## Overview

This repository contains my work for the **JP Morgan Chase & Co. Quantitative Research Job Simulation** hosted on Forage. The simulation consists of **4 tasks**, covering key areas in quantitative finance such as **market forecasting**, **pricing models**, **credit risk analysis**, and **FICO score analysis**. Each task is implemented in a dedicated notebook, and the corresponding datasets are provided.

### Key Features
- **Advanced Implementations:** Beyond the task requirements, I implemented financial models such as **Holt-Winters** (for time series forecasting) and **Logistic Regression** (for credit risk analysis).
- **Documentation:** Task instructions, methodologies, and insights are documented within the notebooks and this README.
- **Datasets:** Includes `Nat_Gas.csv`, `Task3n4_Loan_Data.csv`, and `Nat_Gas_forecast.csv` for Tasks 1, 3, and 4 respectively.

---

## Repository Structure
"""
/
├── Task1_Market_Forecasting/
│ ├── Nat_Gas.csv
│ └── Task1_Market_Forecasting.ipynb
├── Task2_Pricing_Models/
│ ├── Nat_Gas_forecast.csv
│ └── Task2_Pricing_Models.ipynb
├── Task3_Credit_Risk_Analysis/
│ ├── Task3n4_Loan_Data.csv
│ └── Task3_Credit_Risk_Analysis.ipynb
├── Task4_FICO_Score_Analysis/
│ ├── Task3n4_Loan_Data.csv
│ └── Task4_FICO_Score_Analysis.ipynb
└── README.md
"""
---

## Tasks

### Task 1: Market Forecasting - Forecasting Natural Gas Market Price
**Objective:** Analyze historical natural gas price data (`Nat_Gas.csv`) to estimate past prices and forecast prices one year into the future.  
**Approach:**
- Visualized the data to identify trends and seasonal patterns.
- Implemented **Holt-Winters Exponential Smoothing** for time series forecasting.
- Developed a function to take a date as input and return a price estimate.

**Key Insights:**
- Seasonal trends significantly impact natural gas prices.
- The model provides a reliable extrapolation for long-term storage contract pricing.

---

### Task 2: Pricing Models - Pricing Natural Gas Contracts
**Objective:** Develop a prototype pricing model for natural gas contracts using forecasted data (`Nat_Gas_forecast.csv`).  
**Approach:**
- Created a function to price contracts based on injection/withdrawal dates, rates, storage costs, and maximum volume.
- Assumed zero interest rates and no transport delays for simplicity.
- Tested the model with sample inputs to validate its accuracy.

**Key Insights:**
- The model generalizes well for various contract scenarios.
- Manual oversight is recommended before full automation.

---

### Task 3: Credit Risk Analysis - Calculating Probability of Default (PD)
**Objective:** Build a model to predict the probability of default (PD) for loan borrowers using provided data (`Task3n4_Loan_Data.csv`).  
**Approach:**
- Trained a **Logistic Regression** model to estimate PD.
- Incorporated a 10% recovery rate to calculate expected loss.
- Explored additional techniques (e.g., decision trees) for comparative analysis.

**Key Insights:**
- Logistic Regression provided a robust baseline for PD estimation.
- The model can be extended with more advanced techniques for improved accuracy.

---

### Task 4: FICO Score Analysis - Bucketing FICO Scores
**Objective:** Create a rating map to bucket FICO scores into categories, where lower ratings signify better credit scores.  
**Approach:**
- Applied **quantization** techniques to optimize bucket boundaries.
- Explored optimization criteria such as mean squared error and log-likelihood.
- Developed a generalizable approach for future datasets.

**Key Insights:**
- The bucketing strategy effectively summarizes FICO scores for model input.
- The approach can be adapted for different datasets and bucket sizes.

---

## Notes
- The notebooks are provided for better visualization and understanding of the work. Python code prototypes are not included in this repository.
- Task instructions and methodologies are documented within the notebooks and this README.

---

Thank you for visiting! Feel free to reach out with any questions or feedback.
