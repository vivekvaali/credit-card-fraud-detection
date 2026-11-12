# Saved Models

This folder contains the trained machine learning model and its configuration file used for credit card fraud detection.

## Files

### 1. `credit_card_fraud_model_compressed.pkl`
- Compressed, trained Random Forest classification model.
- Used to predict whether a transaction is potentially fraudulent or legitimate.
- Saved using Joblib compression to reduce file size.

### 2. `model_config.pkl`
- Stores the prediction threshold (0.30).
- Contains the feature information required for model predictions.

## Usage

Load the saved files using Joblib:

```python
import joblib

model = joblib.load("models/credit_card_fraud_model_compressed.pkl")
config = joblib.load("models/model_config.pkl")
```

The model and configuration file are used together during prediction.
