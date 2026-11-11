# Credit Card Fraud Detection Using Machine Learning

## Project Overview

This project focuses on identifying potentially fraudulent credit card transactions using Machine Learning.

The objective is to develop a classification model that distinguishes between legitimate and fraudulent transactions based on transaction-related information.

The project includes data preprocessing, exploratory data analysis, feature engineering, class imbalance handling, Random Forest classification and model evaluation.

## Project Objectives

- Analyse credit card transaction data.
- Understand patterns in legitimate and fraudulent transactions.
- Perform data cleaning and preprocessing.
- Handle imbalanced classification.
- Develop a Random Forest classification model.
- Evaluate model performance using appropriate metrics.
- Compare prediction thresholds to improve fraud detection.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Google Colab

## Dataset

This project uses the synthetic Credit Card Fraud Detection dataset published on Kaggle.

**[Download the Credit Card Fraud Detection Dataset from Kaggle](https://www.kaggle.com/datasets/kartik2112/fraud-detection)**

The dataset contains transaction information and a target column named `is_fraud`.

The original CSV files are not included in this repository. Refer to `data/README.md` for download instructions.

## Project Workflow

1. Data loading and understanding
2. Data cleaning and preprocessing
3. Exploratory Data Analysis (EDA)
4. Feature engineering
5. Categorical feature encoding
6. Stratified train-test splitting
7. Random Forest model training
8. Model evaluation
9. Prediction threshold comparison
10. Feature importance analysis
11. Model saving

## Handling Class Imbalance

The dataset contains significantly more legitimate transactions than fraudulent transactions.

To address this imbalance, the Random Forest Classifier uses:

`class_weight='balanced_subsample'`

This assigns greater importance to the minority fraud class during model training.

## Machine Learning Model

**Algorithm:** Random Forest Classifier

The prepared dataset was divided into:

- 80% training data
- 20% testing data

A stratified split was used to maintain the proportion of legitimate and fraudulent transactions in both sets.

## Model Evaluation

The model was evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

### Prediction Threshold Comparison

| Metric | Threshold 0.50 | Threshold 0.30 |
|---|---:|---:|
| Accuracy | 99.81% | 99.83% |
| Precision | 97.55% | 90.80% |
| Recall | 68.89% | 79.55% |
| F1-score | 80.75% | 84.80% |

Reducing the prediction threshold from 0.50 to 0.30 improved recall and F1-score.

The model identified more fraudulent transactions, but also generated more false-positive predictions.

**Evaluation note:** These results are from an internal stratified 80/20 split of the uploaded dataset. The separate Kaggle `fraudTest.csv` file has not yet been used for evaluation.

## Feature Importance

Random Forest feature importance was used to examine the contribution of different input features to model predictions.

Transaction amount and transaction time were among the prominent features in the analysis.

## Saved Model Files

The trained model and its configuration are saved in the `models/` directory.

- `credit_card_fraud_model.pkl` — trained Random Forest model.
- `model_config.pkl` — prediction threshold and feature information.

## How to Run the Project

1. Clone or download this repository.
2. Download the dataset using the Kaggle link above.
3. Follow the instructions in `data/README.md`.
4. Open the notebook in Google Colab or Jupyter Notebook.
5. Upload the required CSV file.
6. Install the dependencies listed in `requirements.txt`.
7. Execute the notebook cells in order.

## Future Improvements

- Evaluate the model using Kaggle's separate testing dataset.
- Explore additional classification algorithms.
- Perform further threshold optimisation using validation data.
- Investigate additional model explainability techniques.

## Author

**Vivek N K**

- GitHub: https://github.com/vivekvaali
- LinkedIn: https://www.linkedin.com/in/vivek-n-k-529101335
