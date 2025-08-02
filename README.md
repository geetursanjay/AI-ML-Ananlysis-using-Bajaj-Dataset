# 📈 Bajaj Finance Stock Price Prediction using Machine Learning

This project aims to predict stock price trends for **Bajaj Finance Ltd** using multiple **machine learning regression techniques**. The goal is to develop a robust predictive model that aids in investment decisions by analyzing historical price movements and technical indicators.

---

## 🧠 Project Objectives

- Analyze stock trends using technical indicators.
- Clean, preprocess, and engineer features from financial data.
- Train multiple ML models and compare their performance.
- Deploy the best-performing model for prediction.

---

## 📊 Dataset Overview

- 📦 Rows: 58,646
- 📌 Columns: 60
- 💡 Features:
  - Price indicators: Open, High, Low, Close
  - Technical indicators: SMA, EMA, ATR, RSI, FastK, FastD
  - Volume
- ✅ Cleaned: Missing values removed, outliers handled (24 rows removed)

---

## 🔧 Tools & Technologies

- Python 3.x
- Jupyter Notebook / Google Colab
- Libraries:
  - pandas, numpy
  - matplotlib, seaborn
  - scikit-learn (sklearn)

---

## 📈 Machine Learning Models Used

| Model                    | Description                                                                 | Highlights                                  |
|-------------------------|-----------------------------------------------------------------------------|---------------------------------------------|
| Linear Regression        | Basic model between Open & Close                                           | Limited by linearity, sensitive to outliers |
| Multiple Linear Regression | Uses Open, High, Low, SMA5, EMA10 as predictors                        | Captures more variance                      |
| Robust Regression (RANSAC, Theil-Sen, Huber) | Outlier-resistant models                            | RANSAC performed best                       |
| Polynomial Regression    | Captures non-linearity in trends                                           | High accuracy, risk of overfitting          |
| Ridge Regression         | Regularized model (L2 penalty)                                             | **Final selected model** (α = 0.001)        |
| Lasso Regression         | Feature selection via L1 regularization                                    | Underperformed due to over-regularization   |

---

## 🧪 Model Evaluation

- ✅ **Final Model**: Ridge Regression
- 📉 **Training MSE**: 15.623
- 📈 **Testing MSE**: 19.202
- 🔢 **R² Score**: 0.99999

---

## 🛠️ How to Run

1. Clone or download the repository
2. Open `bajaj finance project_22csu340.ipynb` in Jupyter or Google Colab
3. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
