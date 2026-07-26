# MSCS 634 Project Deliverable 2

## Regression Modeling and Performance Evaluation

**Student:** Lonnell Johnson

## Project Purpose

The purpose of this project deliverable is to apply feature engineering, regression modeling, model evaluation, and cross-validation techniques to the Online Retail dataset. This phase builds on the cleaned dataset created during Project Deliverable 1.

## Dataset

The project uses the cleaned Online Retail dataset from Project Deliverable 1. The dataset contains retail transaction information including invoice numbers, products, quantities, unit prices, customers, countries, and transaction dates.

For regression analysis, the transaction-level data was transformed into invoice-level data so that the models could predict the total value of customer orders.

## Feature Engineering

Several features were created or transformed for regression modeling. Transaction revenue was calculated using quantity and unit price. Date information was converted into month, day-of-week, and hour features.

The data was then aggregated by invoice to create the following predictive features:

- Total quantity purchased
- Number of unique products
- Average unit price
- Month
- Day of week
- Transaction hour

The target variable was the total monetary value of each invoice.

## Regression Models

Two regression models were developed and compared:

1. Multiple Linear Regression
2. Ridge Regression

Multiple Linear Regression provided a baseline model using all selected features. Ridge Regression introduced L2 regularization to reduce coefficient magnitude and help control overfitting.

## Model Evaluation

The models were evaluated using:

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R-squared (R²)
- Five-fold cross-validation

Lower MAE, MSE, and RMSE values indicate smaller prediction errors, while higher R² values indicate stronger predictive performance.

Five-fold cross-validation was also performed to evaluate how well each model generalized across different portions of the dataset.

## Visualizations

Visualizations were created to examine and compare model performance, including:

- Distribution of invoice totals
- Actual versus predicted values
- R² comparison
- RMSE comparison
- Cross-validation R² comparison
- Regression feature coefficients

## Key Insights

Feature engineering transformed the original transaction records into meaningful invoice-level characteristics that could be used for regression modeling.

Multiple Linear Regression provided a baseline for predicting invoice totals, while Ridge Regression demonstrated how regularization can control model complexity.

The comparison of test-set metrics and cross-validation results provided a broader understanding of model performance and generalization rather than relying on a single evaluation measure.

## Challenges and Decisions

One challenge was determining an appropriate regression target from transaction-level retail data. Invoice total was selected because it represents a meaningful continuous business outcome.

Another challenge was handling the large size and skewed nature of retail transaction values. Aggregating records to the invoice level made the regression problem more meaningful and manageable.

Cross-validation was used in addition to a standard train-test split to provide a more reliable assessment of model performance.

## Repository Contents

- `MSCS_634_ProjectDeliverable_2.ipynb` - Jupyter Notebook containing the complete analysis
- `cleaned_online_retail.csv` - Cleaned dataset from Project Deliverable 1
- `README.md` - Project documentation
- `.gitignore` - Prevents unnecessary environment and temporary files from being uploaded
