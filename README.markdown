# Logistic Regression for Breast Cancer Prediction


## 1. Data Prep
We load the Breast Cancer dataset, split it into training/testing sets, and scale features using StandardScaler.

## 2. Model Training
A LogisticRegression model is trained to predict whether a tumor is malignant (0) or benign (1).

## 3. Evaluation & Threshold Tuning
The model is initially evaluated using a Confusion Matrix, Precision, Recall, and ROC-AUC. Crucially, we then tune the classification threshold (instead of the default 0.5) using the ROC curve to find an optimal point that balances false positives and false negatives, re-evaluating metrics with this new threshold.

## 4. ROC Curve Visualization
A plot of the ROC curve is included to visualize the model's performance across different thresholds.

