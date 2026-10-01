# Deep Learning Financial Forecasting
### Reproduction and Extension of Krauss et al. (2018)

[![Python](https://img.shields.io/badge/Python-3.11-blue.svg)]()
[![Status](https://img.shields.io/badge/Status-Research%20Project-orange.svg)]()

---

## Overview

This repository contains an implementation and partial reproduction of the research paper:

**Krauss, C., Do, X. A., & Huck, N. (2018)**  
*"Deep Neural Networks, Gradient-Boosted Trees, Random Forests, and Logistic Regression for Financial Asset Pricing."*

The objective of this project is to investigate whether machine learning and deep learning models can generate profitable trading signals using historical S&P 500 stock data.

The study compares traditional machine learning methods with deep learning approaches and evaluates their ability to predict future stock movements through a long-short portfolio strategy.

---

## Research Objectives

The main goals of this project are:

- Reproduce the methodology proposed by Krauss et al. (2018)
- Construct the same financial features used in the paper
- Implement benchmark models
- Develop an LSTM-based forecasting framework
- Compare predictive performance and portfolio returns
- Analyze the effectiveness of deep learning in asset pricing

---

## Models Implemented

### Benchmark Models

- Logistic Regression
- Random Forest
- Deep Neural Network (DNN)

### Deep Learning Model

- Long Short-Term Memory (LSTM)

---

## Dataset

### Universe

- S&P 500 Constituents
- Period: 1990 – 2015
- Daily adjusted closing prices
- Historical index membership
- Includes delisted firms when available

### Data Sources

- Yahoo Finance
- Bloomberg Terminal
- Public Financial Databases

---

## Feature Engineering

The project follows the feature construction framework described in Krauss et al. (2018).

### Lagged Return Features

- Return (t−1)
- Return (t−2)
- Return (t−3)
- Return (t−5)
- Return (t−10)
- Return (t−20)
- Return (t−60)

### Additional Features

- Momentum Indicators
- Rolling Volatility Measures
- Normalized Price-Based Features

---

## Experimental Design

### Rolling Window Framework

Training and testing are performed using a rolling-window methodology:

1. Train model on historical data
2. Validate hyperparameters
3. Generate out-of-sample predictions
4. Form long-short portfolios
5. Move window forward
6. Repeat over entire sample

---

## Portfolio Construction

Daily stock rankings are generated using model predictions.

### Long Portfolio

Top K stocks with highest predicted probability

### Short Portfolio

Bottom K stocks with lowest predicted probability

### Evaluation

Long-Short Return:

```
Long Return − Short Return
```

---

## Performance Metrics

### Prediction Metrics

- Accuracy
- Top/Flop Accuracy
- Binomial Test
- Pesaran-Timmermann Test

### Portfolio Metrics

- Mean Return
- Sharpe Ratio
- Sortino Ratio
- Maximum Drawdown
- Value at Risk (VaR)
- Conditional VaR (CVaR)
- Newey-West t-statistics

---

## Repository Structure

```text
Deep-Learning-Financial-Forecasting
│
├── Data/
│   ├── raw/
│   ├── processed/
│
├── Notebooks/
│   ├── Notebook_1_Data_Preparation.ipynb
│   ├── Notebook_2_Feature_Engineering.ipynb
│   ├── Notebook_3_Logistic_Regression.ipynb
│   ├── Notebook_4_Random_Forest.ipynb
│   ├── Notebook_5_DNN.ipynb
│   ├── Notebook_6_LSTM.ipynb
│
├── Outputs/
│   ├── figures/
│   ├── results/
│
├── Reports/
│
├── Research Paper/
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## Environment

### Software

- Python 3.11.16

### Main Libraries

```txt
numpy==2.4.6
pandas==2.2.3
scipy==1.17.1
scikit-learn==1.9.1
matplotlib==3.9.2
yfinance==1.7.0
requests==2.32.3
jupyterlab==4.3.4
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/saharanrahul/Deep-Learning-Financial-Forecasting.git
```

Move into the project directory:

```bash
cd Deep-Learning-Financial-Forecasting
```

Create environment:

```bash
conda create -n stock_lstm python=3.11
conda activate stock_lstm
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Current Progress

### Completed

- Data collection pipeline
- Data preprocessing
- Feature engineering
- Logistic Regression benchmark
- Rolling-window backtesting framework
- Portfolio construction engine
- Performance evaluation framework

### In Progress

- Random Forest implementation
- Deep Neural Network implementation
- LSTM architecture development
- Comparative analysis

---

## Preliminary Findings

The Logistic Regression benchmark shows:

- Out-of-sample prediction accuracy above random guessing
- Statistically significant top/flop stock selection
- Positive long-short portfolio returns
- Evidence that simple machine learning models can extract predictive information from historical price features

---



## Reference

Krauss, C., Do, X. A., & Huck, N. (2018).

*Deep Neural Networks, Gradient-Boosted Trees, Random Forests, and Logistic Regression for Financial Asset Pricing.*

European Journal of Operational Research, 272(2), 689–702.


---

## Disclaimer

This repository is intended for academic and research purposes only.  
It does not constitute financial advice or investment recommendations.
