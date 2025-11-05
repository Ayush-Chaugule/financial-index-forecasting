# Financial Index Forecasting using Regression Models

This repository contains a set of forecasting models built using **Multiple Linear Regression (MLR)**, **Ridge Regression**, and **Lasso Regression** to analyze and predict the returns of  global financial indices.  
Each model is capable of using a  a multivariate dataset of historical market indices, economic indicators, and macroeconomic factors.

## Overview 

The project compares the statistical rigor and predictive performance of regression-based models on **weekly** and **monthly** data frequencies.

| Model Type | Frequency | Focus | Recommended For |
|-------------|------------|--------|----------------|
| **MLR (Multiple Linear Regression)** | Weekly | Deeper statistical analysis (diagnostics, interpretability) | Research & analytical insights |
| **Ridge / Lasso Regression** | Weekly | Regularized regression to reduce overfitting | Research & comparison with MLR |
| **MLR (Multiple Linear Regression)** | Monthly | Simple and fast forecasting | Quick evaluations |
| **Ridge / Lasso Regression** | Monthly | Stable predictive performance with less noise | Quick forecasts with better generalization |


## Data Preprocessing

The notebook **`Data_PreProcessing.ipynb`** is provided for basic data cleaning and merging.
It allows you to:
- Load one or multiple CSVs  
- Merge datasets on a common key (e.g., `Date`)  
- Remove unwanted columns  
- View missing-value summary  

> **Note:**  
> Many official sources (e.g., NSE, Yahoo Finance, FRED, Investing.com) allow direct downloads of **weekly** or **monthly** data.  
> Therefore, this notebook does **not** perform resampling — it assumes your data is already frequency-adjusted.

---

## Model Summaries

### **Weekly Models**
- Offer detailed **statistical analysis** (residual tests, multicollinearity, normality, autocorrelation).  
- Great for **interpretability** and **diagnostics**.  
- Ridge and Lasso versions add **regularization** for better predictive stability.

### **Monthly Models**
- Simpler and faster to run — best for **quick forecasts** or **exploratory work**.  
- Suitable when data volume or detail is lower.

---


## Evaluation Metrics
All models are evaluated on:
- **R² Score (Train/Test)**  
- **RMSE** – Root Mean Squared Error  
- **MAE** – Mean Absolute Error  

### **Residual Analysis & Diagnostic Tests**
- **Shapiro–Wilk** → Normality check  
- **Breusch–Pagan** → Homoskedasticity  
- **Durbin–Watson** → Autocorrelation  
- **VIF** → Multicollinearity  

---

## Forecast Output

Each notebook generates:
- **Actual vs Predicted** plots  
- **Feature importance** charts  
- **Residual & diagnostic** visualizations  
- **Next-period forecasts:**
  - 1-month forecast for monthly models  
  - 1–4-week rolling forecast for weekly models  

---

>  **Disclaimer:**  
> This repository and its contents are created **purely for learning and academic purposes**.  
> The forecasting models here are **not investment tools** and should **not be used for real financial decisions**.  
> Market investments carry inherent risk, and these models are intended only to demonstrate regression-based forecasting techniques.

---

### Additional Note

All work in this project was tested on **Python 3.10**, and results were **consistent and satisfactory**.  
A detailed personal **project report** will be added soon in a `/report` folder.

---

## Setup & Requirements

**Dependencies:**
- Python 3.8+
- pandas
- numpy
- matplotlib
- seaborn
- statsmodels
- scikit-learn
- scipy

Install everything with:
```bash
pip install -r requirements.txt


