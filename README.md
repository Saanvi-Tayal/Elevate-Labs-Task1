# Predicting-Calorie-ExpenditurePreprocessing Steps

## Process of Cleaning the data 
### Explored the Dataset:
Checked data types, missing values, and stats with df.info(), df.head(), and df.describe(). No missing values found.

### Encoded Categorical Data: 
Converted Sex ('male'/'female') to numerical (0/1) using pd.get_dummies(), creating Sex_male (1 for male, 0 for female).

### Standardized Numerical Features: 
Standardized Age, Height, Weight, Duration, Heart_Rate, and Body_Temp using StandardScaler (mean=0, std=1).

### Handled Outliers:
Visualized outliers with boxplots, used IQR method (Q1, Q3, IQR), and capped outliers by setting values outside bounds (Q1-1.5IQR, Q3+1.5IQR) to the bounds, applied to Calories and numerical columns.

## Tools Used

Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn
