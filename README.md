# Crash Prediction in the S&P 500 Using VIX and Market Features

## Overview

This project investigates whether market crashes in the S&P 500 can be predicted using information derived from the CBOE Volatility Index (VIX), market returns, volatility measures, and technical indicators.

The objective is not to perfectly forecast crashes, but to evaluate whether statistically significant signals exist before large market declines and whether machine learning models can exploit these signals.

The project was developed as a final exam project for the SoftUni Mathematics for Developers course.

---

## Research Question

Can future market crashes in the S&P 500 be predicted using VIX-based features and historical market behavior?

More specifically:

* Can periods of elevated market fear (high VIX) improve crash prediction?
* Which features provide the strongest predictive signal?
* How do different machine learning models compare?
* What are the practical limitations of crash prediction?

---

## Dataset

The project uses historical market data including:

* S&P 500 prices
* VIX index values
* Derived return features
* Rolling volatility measures
* Technical indicators
* Lagged market information

Crash events are defined according to a predefined threshold of future market decline within a selected prediction horizon.

---

## Methodology

### Data Preparation

The following steps were performed:

1. Data collection and alignment
2. Missing value handling
3. Feature engineering
4. Crash label generation
5. Train-test splitting with temporal integrity

Special attention was given to preventing data leakage.

---

### Feature Engineering

Examples of engineered features include:

* Daily returns
* Rolling returns
* VIX levels
* VIX changes
* Rolling volatility
* Moving averages
* Relative market strength measures
* Lagged indicators

---

### Models Evaluated

The following models were trained and compared:

1. Logistic Regression
2. Random Forest
3. XGBoost

Model performance was evaluated using time-series aware validation procedures.

---

### Validation Strategy

A walk-forward validation framework was used to better simulate real-world forecasting conditions.

This approach ensures that:

* Future information is never used during training.
* Model evaluation reflects realistic deployment.
* Data leakage is minimized.

---

## Evaluation Metrics

The models were evaluated using:

* Precision
* Recall
* F1 Score
* ROC-AUC
* Confusion Matrix

Because crash prediction is an imbalanced classification problem, special emphasis was placed on Recall and F1 Score rather than simple accuracy.

---

## Results

The experiments demonstrate that:

* Predicting crashes remains a difficult task.
* VIX contains useful information regarding future market stress.
* Some predictive signal exists, but performance is limited.
* Ensemble methods generally outperform simpler linear models.
* False positives remain a significant challenge.

The findings are consistent with existing financial literature suggesting that market crashes are inherently difficult to forecast.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* XGBoost
* Jupyter Notebook


---

## Future Improvements

Potential extensions include:

* Additional macroeconomic indicators
* Interest rate data
* Credit spreads
* Alternative crash definitions
* Deep learning architectures
* Probabilistic forecasting methods
* Explainable AI techniques (SHAP, LIME)

---

## References

* CBOE Volatility Index (VIX) documentation
* Scikit-Learn documentation
* XGBoost documentation
* Academic literature on financial crisis prediction and volatility forecasting


