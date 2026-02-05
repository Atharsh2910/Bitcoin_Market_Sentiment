# Fear & Greed Index Analysis Using Machine Learning

## Project Overview
In this project, I analysed the Fear & Greed Index using a combination of supervised learning, unsupervised learning, and regression techniques to understand market sentiment behaviour. The objective was to classify sentiment correctly, avoid overfitting, explain model decisions, and forecast short-term sentiment trends in a methodologically sound and interpretable manner.

---

## How to Run the Notebook

### Requirements
- Python 3.9 or above

Install required libraries:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost shap catboost
```

---

## Steps to Run

Clone the repository

Open Jupyter Notebook or JupyterLab

Open the .ipynb file

Run the notebook cells sequentially from top to bottom

## Dataset Description

The dataset contains the following columns:

timestamp – time of observation

date – date of observation

value – Fear & Greed Index value

classification – sentiment label (Fear / Neutral / Greed)

## Methodology and Approach
# 1. Data Preprocessing

Checked dataset dimensions, missing values, and duplicates

Converted timestamp and date fields into proper datetime formats

Removed NaN and infinite values to ensure numerical stability

Ensured clean and consistent input for all models

# 2. Supervised Classification

Initially trained Random Forest, XGBoost, and CatBoost classifiers

Observed evaluation metrics were perfect 1. So it was overfitted.


# 3. Model Improvisation and Selection

Reduced model complexity by switching to Logistic Regression

Logistic Regression produced realistic and stable metrics

The model generalised better and avoided memorisation

Selected Logistic Regression as the final classifier based on reliability

# 4. Classification Explainability and Visualisation

Used confusion matrix to evaluate class-wise performance

Plotted ROC curves for multiclass evaluation

Applied PCA to visualise class separation

Analysed model coefficients for interpretability

Used SHAP values to understand feature importance

# 5. Unsupervised Learning (K-Means Clustering)

Applied K-Means clustering to identify sentiment regimes

Used WCSS (Inertia) and the Elbow Method to choose the optimal number of clusters

Evaluated clustering using Silhouette Score and Calinski-Harabasz Index

Observed clusters aligning with Fear, Neutral, and Greed sentiment periods

# 6. Regression and Forecasting

Trained an XGBoost regression model

Target variable was the Fear & Greed Index value

Used time-based and sentiment-based features

Evaluated performance using Mean Squared Error (MSE) and Mean Absolute Error (MAE)

Forecasted sentiment values for the next six days

# 7. Visualisation

Compared actual vs predicted sentiment trends

Analysed residuals to verify model stability

Visualised index distribution to ensure realism

Highlighted sentiment regime zones over time

Visualised six-day forecast trend

Created an executive summary chart for final sentiment interpretation

# 8. Final Conclusions

Logistic Regression provides the most reliable and interpretable classification

Fear & Greed Index exhibits clear and consistent sentiment regimes

K-Means clustering independently validates sentiment structure

Fear periods generally indicate accumulation opportunities

Greed periods indicate higher risk and potential profit booking

XGBoost regression offers a reasonable short-term sentiment forecast
