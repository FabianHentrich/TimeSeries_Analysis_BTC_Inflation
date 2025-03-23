# 📈 Inflation and Bitcoin: A Time-Series VAR Analysis

This project replicates and tests the robustness of the findings from the paper:  
> **Blau, B. M., Griffith, T. G., & Whitby, R. J. (2021). Inflation and Bitcoin: A descriptive time-series analysis. _Economics Letters_, 203, 109848.**

The goal is to explore the dynamic relationship between Bitcoin returns and inflation expectations (measured by T5YIFR) using Vector Autoregression (VAR) models across multiple time periods.

---

## 📚 Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Time Periods Analyzed](#time-periods-analyzed)
- [Results](#results)
- [Conclusion](#conclusion)
- [How to Run](#how-to-run)
- [Dependencies](#dependencies)

---

## 📊 Project Overview

This analysis investigates whether Bitcoin acts as a hedge against inflation by analyzing the relationship between:
- **Bitcoin returns (BTC-USD)**  
- **U.S. inflation expectations (T5YIFR)**  

---

## 📂 Dataset

- **Bitcoin Prices**: Daily closing prices from Yahoo Finance (BTC-USD).  
- **Inflation Expectations (T5YIFR)**: Daily data from the Federal Reserve Bank of St. Louis (FRED).

---

## ⚙️ Methodology

The analysis replicates the VAR methodology used in the original paper and includes:

1. **Data Preprocessing**:
   - Log-differencing of Bitcoin prices to obtain returns.
   - Filtering by selected timeframes.
   - Stationarity testing using the Augmented Dickey-Fuller (ADF) test.

2. **Model Specification**:
   - Vector Autoregression (VAR) model with lag selection based on AIC, BIC, and HQIC.
   - Granger causality tests.
   - Impulse Response Functions (IRFs).
   - Forecast Error Variance Decomposition (FEVD).
   - Cointegration testing.

---

## 🕒 Time Periods Analyzed

This analysis examines three distinct timeframes to test for robustness and consistency:  
- **2015–2018**  
- **2019–2020** (Reproduction of Blau et al. (2021))  
- **2022–2024**

---

## ✅ Results

### **Key Findings Across Time Periods**
- **Time Period 2015–2018**:
  - **Granger Causality**: The Engle-Granger test revealed no relationship between Bitcoin returns and inflation expectations. There was no significant Granger causality in either direction.
  - **IRFs**: The Impulse Response Functions (IRFs) showed that neither inflation nor Bitcoin returns significantly affect each other.

- **Time Period 2019–2020** (Reproduction of the original paper):
  - **Granger Causality**: The analysis found that Bitcoin prices Granger-cause expected inflation, but not the other way around, suggesting that Bitcoin can act as an inflation hedge.
  - **IRFs**: The IRFs show that Bitcoin has a significant mid- to long-term effect on expected inflation, which stabilizes around 0.15.

- **Time Period 2022–2024**:
  - **Granger Causality**: The results in this period were opposite to those found by the authors: Expected inflation rate Granger-causes Bitcoin price, but not vice versa.
  - **IRFs**: We observed a possible long-term effect of expected inflation on Bitcoin price. However, the cumulative impulse response for 40 periods showed high variance, preventing us from confirming this relationship with certainty.

---

## 🔎 Conclusion

➡️ The results consistently suggest that **Bitcoin does not act as a reliable hedge against inflation** across the analyzed time periods. Despite differing the different time periods, the relationship between Bitcoin and inflation expectations remains weak and statistically insignificant.  
These findings imply that Bitcoin may not serve as an effective hedge against inflation.
This consistent finding reinforces the conclusion of the original study by Blau et al. (2021), but extends the analysis to additional periods for enhanced robustness.

