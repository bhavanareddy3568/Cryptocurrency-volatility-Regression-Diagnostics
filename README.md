# ₿ Cryptocurrency Volatility Analysis using Regression Diagnostics

An end-to-end statistical analysis project focused on understanding and modeling Bitcoin volatility using regression diagnostics, financial market indicators, and feature engineering techniques.

----

## 📌 Project Overview

Cryptocurrency markets are highly volatile and influenced by numerous factors including trading activity, investor sentiment, market trends, and macroeconomic conditions.

This project investigates the drivers of Bitcoin volatility by developing and improving multiple linear regression models and evaluating model assumptions through comprehensive regression diagnostics.

The objective was not only to predict Bitcoin returns but also to understand:

* What factors influence Bitcoin volatility
* Whether traditional regression assumptions hold for financial data
* How feature engineering impacts model performance
* Which variables provide the strongest explanatory power

----

## 🎯 Business Problem

Investors, traders, and financial analysts need reliable methods to understand cryptocurrency price behavior and risk.

Bitcoin markets often experience:

* Extreme price fluctuations
* Market uncertainty
* Speculative trading behavior
* High sensitivity to external events

The challenge is to identify statistically significant factors affecting Bitcoin volatility while ensuring the reliability of predictive models through rigorous diagnostic testing.

----

## 📊 Dataset

### Source

Yahoo Finance Historical Market Data

### Time Period

2014 – 2025

### Variables Used

* Open Price
* High Price
* Low Price
* Close Price
* Trading Volume
* S&P 500 Closing Prices

----

## 🧹 Data Preparation & Feature Engineering

Performed extensive preprocessing and transformation activities:

### ✅ Data Cleaning

* Removed missing values
* Corrected datatype inconsistencies
* Merged Bitcoin and S&P 500 datasets
* Eliminated duplicate records

### ✅ Return Calculations

Calculated:

* Bitcoin Log Returns
* S&P 500 Log Returns

Formula:

Log Return = ln(Pt / Pt-1)

### ✅ Outlier Handling

* Z-Score Analysis
* Regression Influence Diagnostics
* Cook’s Distance Analysis

### ✅ Volume Transformation

Applied logarithmic transformation to trading volume to reduce skewness and improve model stability.

----

## 🔬 Initial Regression Model

### Target Variable

Bitcoin Log Returns

### Predictor Variables

* S&P 500 Log Returns
* Trading Volume

### Model

Multiple Linear Regression (OLS)

BTC Return = β0 + β1(S&P Return) + β2(Volume) + ε

----

## 📈 Regression Diagnostics

Comprehensive diagnostic testing was performed to evaluate model assumptions.

### Residual Analysis

* Residual vs Fitted Plot
* Homoscedasticity Assessment

### Normality Testing

* Q-Q Plot Analysis

### Multicollinearity

Variance Inflation Factor (VIF)

VIF ≈ 1

### Result:

* No significant multicollinearity detected

### Autocorrelation

Durbin-Watson Statistic

Durbin-Watson = 1.68

### Interpretation:

* Mild positive autocorrelation
* Indicates presence of time-series dependencies

### Influential Observations

Cook’s Distance

Used to identify observations with excessive influence on model coefficients.

----

## ⚙️ Model Improvement Strategy

The initial model showed limited explanatory power.

To improve performance, external noisy variables were reduced and Bitcoin-centric features were engineered.

### Added Features

📈 Lagged Bitcoin Returns

* Captures autocorrelation patterns

📊 Log Trading Volume

* Reflects market participation

📉 Rolling Volatility

* Measures historical return variability

📈 Trend Indicator

* Moving-average-based trend signal

📅 Weekly Aggregation

* Reduced daily noise
* Improved model stability

----

## 🚀 Improved Model

### Final Predictors

* Log Volume
* Lagged Returns
* Rolling Volatility
* Trend Score

### Performance Improvement

Initial Model:

R² ≈ 0.26

Improved Model:

R² ≈ 0.29

The refined model demonstrated improved interpretability and stability while maintaining statistical validity.

----

## 📊 Key Findings

📈 Trend Matters

Bitcoin trend indicators showed meaningful influence on short-term returns.

🔄 Historical Behavior Matters

Lagged returns contributed useful predictive information.

📊 Volume Matters

Trading activity remains one of the strongest indicators of volatility.

🎯 Feature Selection Matters

Removing irrelevant variables improved model performance and interpretability.

⚠️ Market Complexity

### Bitcoin volatility is influenced by:

* Investor sentiment
* Market psychology
* Regulatory announcements
* Macroeconomic conditions
* Social media activity

This explains why financial prediction remains challenging despite statistical modeling.

----

## 💡 Business Impact

### This analysis helps:

Investment Analysts

* Understand volatility drivers
* Evaluate market risk

Traders

* Monitor market activity indicators
* Identify periods of abnormal volatility

Financial Researchers

* Assess model assumptions in financial datasets
* Explore feature engineering techniques

Data Scientists

* Apply regression diagnostics to real-world time-series problems

----

## 🛠️ Technologies Used

### Programming

* Python

### Libraries

* Pandas
* NumPy
* Matplotlib
* Seaborn
* Statsmodels
* Scikit-learn
* SciPy
* yFinance

### Statistical Techniques

* Multiple Linear Regression
* Regression Diagnostics
* VIF Analysis
* Durbin-Watson Test
* Cook’s Distance
* Feature Engineering
* Time-Series Analysis

----

## 📂 Repository Structure

```text
Cryptocurrency-Volatility-Regression-Diagnostics
│
├── Notebooks/
│   └── Crypto_Volatility_Analysis.ipynb
│
├── Reports/
│   ├── Project_Proposal.pdf
│   └── crypto_volatility_presentation.pptx
│
├── Screenshots/
│   ├── residual_plot.png
│   ├── qq_plot.png
│   ├── cooks_distance.png
│   └── model_summary.png
│
├── Requirements.txt
└── README.md
```

----

## 📚 Academic Context

Developed as part of graduate-level statistical coursework at Florida State University.

The project combines financial analytics, statistical modeling, and regression diagnostics to investigate cryptocurrency market behavior using real-world financial data.

----

## 👤 Author

### Bhavana Bajjuri

Data Analytics | Statistics | Machine Learning | Business Intelligence

Feel free to connect and provide feedback on the project.
