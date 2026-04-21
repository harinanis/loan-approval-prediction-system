# Intelligent Loan Approval Prediction System

A production-style Streamlit application for predicting loan approval with an interactive dashboard, modern UI, model benchmarking, and explainable analytics.

## Project Overview

This app:
- Trains three ML models on `train.csv` (`Logistic Regression`, `Decision Tree`, `XGBoost`)
- Evaluates performance on `test.csv` (when `Loan_Status` exists)
- Predicts approval for custom applicant inputs from a smart sidebar
- Displays rich Plotly visuals (accuracy comparison, ROC curves, confusion matrix, feature importance, class distribution)
- Provides advanced output cards (animated approval/rejection result, risk gauge, risk category, explanation panel)
- Exports prediction output as CSV

## Dataset Requirements

Place these files in the project root:
- `train.csv`
- `test.csv`

Expected target column:
- `Loan_Status`

Preprocessing rules implemented:
- Drop `Loan_ID`
- Numeric missing values -> mean imputation
- Categorical missing values -> mode imputation
- Label encode categorical features and target
- Reuse fitted imputers/encoders for user predictions

## Local Setup

1. Create and activate a virtual environment (recommended)
2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Run the app:

```bash
streamlit run app.py
```

## Deployment on Streamlit Cloud

1. Push this project to a GitHub repository.
2. Ensure these files are committed:
   - `app.py`
   - `requirements.txt`
   - `README.md`
   - `train.csv`
   - `test.csv`
3. Go to [Streamlit Community Cloud](https://share.streamlit.io/).
4. Click **New app** and select your repository, branch, and `app.py`.
5. Deploy the app.

## App Sections

- **Dashboard Header**: Title and product-style description
- **Data Insights Panel**: Dataset distribution and profile summary
- **Model Performance Panel**: Accuracy, ROC, confusion matrix, feature importance
- **Prediction Panel**: Decision card, probability gauge, risk level, explanation and CSV download

## Notes

- If `Loan_Status` is missing in `test.csv`, the app will skip evaluation metrics and still support prediction.
- For local reproducibility, models are trained directly at runtime using the loaded data.

## Features
- Loan prediction
- Risk analysis

## Author
HarshaVardhan
