
# Breast Cancer Classification with Support Vector Machines (SVMs)
This project demonstrates the process of building and evaluating Support Vector Machine (SVM) models for binary classification using the well-known Breast Cancer Wisconsin (Diagnostic) dataset.

## Project Steps:
 
1. **Data Loading and Preparation:**

* Loaded the Breast Cancer dataset from scikit-learn.
* Split the data into training and testing sets to evaluate model performance on unseen data.
* Standardized the features (scaled them to a common range) using StandardScaler. This is crucial for SVMs as they are sensitive to feature scales.

2. ** SVM Model Training:** 

* Trained two initial SVM models:
* One with a Linear Kernel: Suitable for linearly separable data.
* One with an RBF (Radial Basis Function) Kernel: Effective for non-linearly separable data by implicitly mapping it to a higher-dimensional space.
3. **Decision Boundary Visualization (2D):** 

* Used Principal Component Analysis (PCA) to reduce the dataset's features to just two dimensions.
* Trained an RBF SVM on this 2D data.
* Visualized the model's decision boundary on a plot, showing how the SVM separates the two classes (malignant vs. benign) in a simplified 2D representation.

4. ** Hyperparameter Tuning with GridSearchCV: ** 

* Performed hyperparameter tuning to find the optimal settings for the RBF kernel SVM.
* Used GridSearchCV to systematically search for the best combination of the C parameter (regularization strength) and the gamma parameter (RBF kernel coefficient, controlling influence spread). This helps prevent overfitting and underfitting.

5. ** Cross-Validation for Robust Evaluation: **


* Applied stratified k-fold cross-validation to evaluate the performance of the best-tuned SVM model.
* Cross-validation provides a more reliable estimate of the model's generalization ability by training and testing on multiple different subsets of the data, reducing reliance on a single train-test split.

---

**Technologies Used:**

* **Python**
* **pandas** (for data manipulation)
* **scikit-learn** (for machine learning models, preprocessing, and evaluation)
* **matplotlib** (for plotting and visualization)
* **seaborn** (for enhanced plot aesthetics)
