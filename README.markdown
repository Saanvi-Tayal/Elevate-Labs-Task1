# House Price Prediction with Linear Regression

## Overview
This project predicts house prices using linear regression. It includes data preprocessing, model training, evaluation (MAE, MSE, R²), and visualization of actual vs. predicted values.

## Requirements
- Python 3.x
- Libraries: pandas, numpy, scikit-learn, matplotlib, seaborn


## Files
- `house_price_prediction.py`: Main script with preprocessing, model training, evaluation, and visualization.
- `house_data.csv`: Sample dataset (not included; provide your own).

## Steps Performed
1. **Preprocessing**:
   - Loaded the dataset and handled missing values (numerical with median, categorical with mode).
   - Encoded categorical variables using one-hot encoding.
   - Scaled numerical features (`area`, `bedrooms`, etc.) using `StandardScaler`.
   - Fixed a scaling error by ensuring a 2D DataFrame input to `fit_transform`.

2. **Correlation Visualization**:
   - Computed the correlation matrix with `df.corr()`.
   - Plotted a heatmap using Seaborn to visualize feature correlations.

3. **Model Fitting**:
   - Split data into training (80%) and testing (20%) sets.
   - Fitted a `LinearRegression` model using `sklearn.linear_model`.

4. **Model Evaluation**:
   - Evaluated the model using MAE, MSE, and R² metrics to measure performance.

5. **Visualization**:
   - Plotted actual (blue) and predicted (red) prices against `area` using scatter plots.
   - Added a green regression line to show the model’s predictions.


## Results
The script outputs model evaluation metrics (MAE, MSE, R²) and a plot showing actual vs. predicted prices
