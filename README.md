# COVID-19 Stock Market Analysis Using PCA

This repository contains the code and analysis behind the paper **"Historical Analysis of the S&P 500 During the COVID Period Using PCA"** by Carlos Gafa’. The project explores how Principal Component Analysis (PCA) can be used to identify stock and sector groupings that would have outperformed the S&P 500 during the COVID-19 recession.

## Project Summary

Using historical stock data from the S&P 500 (2019–2021), this analysis investigates:

- How PCA can extract meaningful components representing overall market movement.
- How secondary and tertiary components reveal sectoral and stock-specific behaviors.
- Portfolio construction strategies based on PCA components that outperform the S&P 500 on a risk-adjusted basis.

## Data

- **Source**: [Yahoo Finance](https://finance.yahoo.com/)
- **Period**: January 2019 – December 2021
- **Universe**: 402 S&P 500 stocks that were continuously listed during the period.

## Tools and Libraries

- Python
- `pandas`, `numpy`
- `yfinance` (for data retrieval)
- `scikit-learn` (for PCA)
- `matplotlib`, `seaborn` (for visualization)

## Methodology

1. **Data Normalization**: Log returns were calculated and standardized.
2. **PCA Application**: PCA was applied to the entire period and the COVID-only period (Mar 2020–Dec 2021).
3. **Component Interpretation**:
   - **1st Principal Component**: Identified as the market factor; highly correlated with S&P 500.
   - **2nd Component**: Separated resilient Consumer Defensive stocks from more volatile sectors.
   - **3rd Component**: Highlighted the outperformance of large-cap tech firms (Amazon, Meta, Microsoft, etc.).

## 📈 Results Summary

| Portfolio | Annualized Return | Volatility | Sharpe Ratio | Max Drawdown |
|-----------|-------------------|------------|---------------|---------------|
| S&P 500   | 20.55%            | 22.75%     | 0.90          | 33.92%        |
| 2nd PC (Positive) | 21.55%   | 19.91%     | 1.08          | 26.81%        |
| 3rd PC (Negative) | 29.00%   | 25.45%     | 1.14          | 36.17%        |

The PCA-based portfolios demonstrated potential for risk-adjusted outperformance, with some offering lower drawdown and volatility.

Detailed Writeup and Disuccsion in PDF file.

